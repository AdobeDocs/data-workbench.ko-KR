---
description: 이제 DeviceAtlas JSON 파일은 DeviceAtlas.dll 및 DeviceAtlas64.dll 파일과 함께 .bundle 파일(이름이 .tar.gz)로 배포됩니다.
solution: Analytics
title: DeviceAtlas 배포
topic: Data workbench
uuid: 1eb76c61-6696-4e6c-a3fd-61c00cc17b0a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# DeviceAtlas 배포{#deviceatlas-distribution}

이제 DeviceAtlas JSON 파일은 DeviceAtlas.dll 및 DeviceAtlas64.dll 파일과 함께 .bundle 파일(이름이 .tar.gz)로 배포됩니다.

관리자가 Insight Server를 버전 6.0으로 업그레이드하면 DeviceAtlas.bundle 파일이 다음 위치에 있는 소프트웨어 및 문서 프로필(softdocs 프로필)의 업그레이드 패키지에 포함됩니다.

[!DNL Server Packages > v6.00 > Server_6.00.zip]

DeviceAtlas.bundle 파일의 압축을 [!DNL Server\Lookups\DeviceAtlas]해제했습니다.

DeviceAtlas.bundle 파일은 DPU와 동기화된 디렉토리에 저장해야 하며, 새 DeviceAtlasComponent에 해당하는 DeviceAtlas.cfg 파일은 동기화 마스터의 &quot;처리 서버용 구성 요소&quot; 디렉토리에 저장해야 합니다. DeviceAtlas.bundle 파일이 변경되면 바로 다음 DeviceAtlas 조회 호출은 업데이트된 API 및/또는 JSON 파일을 기준으로 결과를 가져옵니다.

## Transformation.cfg 파일 수정 {#section-394823348f5740028666e62e2bd42754}

DeviceAtlas 변환은 더 이상 JSON 파일의 경로를 지정할 필요가 없습니다. transformation.cfg 파일에 정의된 모든 이전 DeviceAtlasTransformation에는 난독화된 JSON 파일을 가리키는 File 매개 변수가 더 이상 포함되지 않아야 합니다.

이 예제 Transformation.cfg 파일은 혼동을 방지하기 위해 삭제해야 하는 File 인수를 보여줍니다. (그것을 그대로 두면, 해가 생기지는 않고, 그것이 무시되기 때문에 잠재적인 혼란만 야기시킬 것입니다.)

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

이것은 DeviceAtlas.cfg 파일에 필요한 [!DNL component] 인수의 예입니다.

```
component = DeviceAtlasComponent: 
  DeviceAtlas Bundle File = string:Lookups\\DeviceAtlas\\DeviceAtlas.bundle 
  Unsynchronized Bundle Extraction Path = string: Temp\\DeviceAtlas\\
```

이 DeviceAtlas.bundle 파일은 프로필 동기화 기능의 관점에서 구성 파일처럼 처리됩니다. 또한 JSON 데이터 및 DLL은 개별 변형 수준이 아닌 구성 요소 수준에서 사용됩니다.

새 DeviceAtlasComponent는 시작 시 .bundle 복합체를 찾고, JSON 파일을 메모리로 추출하고, 파일을 임시 디렉토리로 추출하고, 실행 중인 플랫폼에 적합한 DLL을 로드합니다. 또한 이 구성 요소는 번들 파일의 변경 사항을 모니터링하고 DLL 및 .cfg 파일이 변경되면 자동으로 다시 로드합니다.

## DeviceAtlas 실행 {#section-6ed37b39199d4ffd95d30b49a7ee9666}

올바른 구성을 통해 변환 시 필요한 시간을 크게 단축할 수 있습니다. 변환은 DeviceAtlas가 프로세스를 가속화할 수 있도록 세션당 방문자당 한 번만 실행하도록 구성할 수 있습니다.

**Log Processing.cfg를 사용하여 배포하는 경우**:

변형을 두 번 실행합니다.

1. 필드만 [!DNL mobile id] 찾아보고
1. 조건을 만들어 [!DNL mobile id] 무시하고 나머지 필드를 조회합니다.

**Transformation.cfg를 사용하여 배포하는 경우**:

위의 로그 처리에서 1단계에서처럼 배포하거나, 행간 을 사용하여 조건부 설정을 지원합니다.

* 행 간 - 이전 세션 키를 선택합니다. 그런 다음 현재 세션 키가 행 간에 있는 세션 키와 다른지 확인합니다. 이 경우 DeviceAtlas 변환은 세션당 한 레코드에서만 실행됩니다.

