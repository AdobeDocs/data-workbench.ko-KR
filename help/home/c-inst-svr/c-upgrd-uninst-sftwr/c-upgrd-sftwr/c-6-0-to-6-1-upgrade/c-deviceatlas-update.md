---
description: 이제 DeviceAtlas JSON 파일이 DeviceAtlas.dll 및 DeviceAtlas64.dll 파일과 함께 .bundle 파일(이름이 변경된 .tar.gz)로 배포됩니다.
title: DeviceAtlas 배포
uuid: 1eb76c61-6696-4e6c-a3fd-61c00cc17b0a
exl-id: e9671810-d32c-4ec4-a1cb-54b71c6f101c,333507bb-3e8b-4da1-8218-b35fcf8d5f80,aa811c7b-ef80-4f23-b395-0cbb7d2677a9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# DeviceAtlas 배포{#deviceatlas-distribution}

{{eol}}

이제 DeviceAtlas JSON 파일이 DeviceAtlas.dll 및 DeviceAtlas64.dll 파일과 함께 .bundle 파일(이름이 변경된 .tar.gz)로 배포됩니다.

관리자가 Insight Server를 버전 6.0으로 업그레이드할 때 DeviceAtlas.bundle 파일은 다음 위치에 있는 소프트웨어 및 문서 프로필(softdocs 프로필)에 있는 업그레이드 패키지에 포함됩니다.

[!DNL Server Packages > v6.00 > Server_6.00.zip]

DeviceAtlas.bundle 파일은 로 추출됩니다 [!DNL Server\Lookups\DeviceAtlas].

DeviceAtlas.bundle 파일은 DPU에 동기화된 디렉터리에 배치해야 하며 새 DeviceAtlasComponent에 해당하는 DeviceAtlas.cfg 파일은 동기화 마스터의 &quot;처리 서버용 구성 요소&quot; 디렉토리에 저장해야 합니다. DeviceAtlas.bundle 파일이 변경되면 바로 다음 DeviceAtlas 조회 호출에서 업데이트된 API 및/또는 JSON 파일을 기반으로 결과를 가져옵니다.

## Transformation.cfg 파일을 수정합니다 {#section-394823348f5740028666e62e2bd42754}

DeviceAtlas 변환에서는 더 이상 JSON 파일의 경로를 지정할 필요가 없습니다. transformation.cfg 파일에 정의된 이전 DeviceAtlasTransformation에는 더 이상 난독화된 JSON 파일을 가리키는 File 매개 변수가 포함되지 않아야 합니다.

이 예제 Transformation.cfg 파일은 혼동을 방지하기 위해 삭제해야 하는 File 인수를 보여줍니다. (그 곳에 두면 아무런 해가 없고, 장차 무시할 것이기 때문에 잠재적인 혼란만 일으킬 뿐이다.)

```
6 = DeviceAtlasTransformation:  
  Comments = Comment: 0 items  
  Condition = AndCondition: 0 items

<b></b> 
<filepath>
  File = string: Lookups\\DeviceAtlas\\20110106_private.json.obfuscated 
</filepath> 
  ^^ DELETE THE ABOVE LINE FROM ALL PREVIOUS TRANSFORMATIONS ^^  
 
  Name = string: DeviceAtlas Lookup  
  Outputs = vector: 4 items  
    0 = Column:  
      Column Name = string: vendor  
      Field Name = string: x-vendor  
    1 = Column:  
      Column Name = string: model  
      Field Name = string: x-model  
    2 = Column:  
      Column Name = string: isBrowser  
      Field Name = string: x-isbrowser  
    3 = Column:  
      Column Name = string:usableDisplayHeight  
      Field Name = string: x-usable-display-height 
User Agent = string: x-ua  
```

## DeviceAtlas.cfg 파일 수정 {#section-10b43705a6c846fd9ec54ea6be249f88}

이 예는 다음과 같습니다 [!DNL component] DeviceAtlas.cfg 파일에 필요한 인수입니다.

```
component = DeviceAtlasComponent: 
  DeviceAtlas Bundle File = string:Lookups\\DeviceAtlas\\DeviceAtlas.bundle 
  Unsynchronized Bundle Extraction Path = string: Temp\\DeviceAtlas\\
```

이 DeviceAtlas.bundle 파일은 프로필 동기화 기능의 관점에서 구성 파일처럼 처리됩니다. 또한 JSON 데이터 및 DLL은 개별 변형 수준이 아닌 구성 요소 수준에서 사용됩니다.

새 DeviceAtlasComponent는 시작 시 .bundle 복합체를 찾아 JSON 파일을 메모리로 난독화하고 파일을 임시 디렉토리에 추출하며 실행 중인 플랫폼에 적절한 DLL을 로드합니다. 또한 이 구성 요소는 번들 파일의 변경 사항을 모니터링하고 DLL 및 .cfg 파일이 변경되면 자동으로 다시 로드합니다.

## DeviceAtlas 실행 {#section-6ed37b39199d4ffd95d30b49a7ee9666}

올바른 구성으로 변환에 필요한 시간이 크게 달라집니다. 변환은 DeviceAtlas가 프로세스 속도를 높일 수 있도록 세션당 방문자당 한 번만 실행되도록 구성할 수 있습니다.

**Log Processing.cfg를 사용하여 배포되는 경우**:

변형을 두 번 실행합니다.

1. 조회 전용 [!DNL mobile id] 그런 다음
1. 무시할 조건 만들기 [!DNL mobile id] 그런 다음 나머지 필드를 찾아봅니다.

**Transformation.cfg를 사용하여 배포되는 경우**:

위의 로그 처리에서 1단계처럼 배포하거나 교차 행을 사용하여 조건부 설정을 지원합니다.

* 교차 행 - 이전 세션 키를 선택합니다. 그런 다음 현재 세션 키가 교차 행이 있는 세션 키와 다른지 확인합니다. 이 경우 DeviceAtlas 변환은 세션당 한 레코드에서만 실행됩니다.
