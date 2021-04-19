---
description: 클라이언트와 서버 간 통신하는 경우 암호와 기타 문자열을 암호화합니다.
title: 문자열 암호화
uuid: b2ec6a10-136c-4694-a425-04dbb41d43d1
exl-id: 43696ff1-3153-4d85-b9a9-c2752dd2c29a
translation-type: ht
source-git-commit: 233b04c65a45d3f92b8670bc244b907dc198b51d
workflow-type: ht
source-wordcount: '268'
ht-degree: 100%

---

# 문자열 암호화{#string-encryption}

클라이언트와 서버 간 통신하는 경우 암호와 기타 문자열을 암호화합니다.

Data Workbench 클라이언트(워크스테이션)와 서버 간 통신하는 경우 *EncryptedString* 유형이 포함된 값 매개 변수(암호 등)를 저장할 수 있습니다. 해당 키가 반환되면 매개 변수를 숨기고 서버측 *Windows Credential Store* 에 문자열을 저장합니다. 내보내기에 사용되는 자격 증명이 일차적으로 저장되지만 매개 변수를 암호화하는 데 사용될 수 있습니다.

* Server\**EncryptStrings**에 새 폴더가 추가되었습니다.

   여기에서 구성 파일을 설정하여 문자열을 암호화합니다.

* Server\Component\**EncryptedStrings.cfg**에 새 구성 파일이 추가되었습니다.

   ```
   component = EncryptionComponent:
     Path = Path: EncryptStrings\\*.cfg
   ```

   이 파일은 암호화 구성 파일의 *Server*\*EncryptStrings* 폴더를 폴링합니다.

**문자열을 암호화하려면**

1. 이들 필드가 설정되면 문자열의 **EncryptedStrings.cfg** 구성 파일을 생성합니다.

   ```
   Names = vector: 1 items
    0 = NameEncryptValuePair:
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server
     Name = string: // Name for identifier 
     Value = string: // Value to be encrypted
   ```

   * *Value* - 이 필드에는 암호화될 일반 텍스트 문자열이 포함됩니다.

      서버측 암호화전용입니다. *Value* 설정은 서버 컴퓨터에서만 암호화됩니다.

   * *Name* - 이 필드에는 암호화된 문자열을 식별하는 값이 포함됩니다.
   * *EncryptValue* - 이 필드는 입력 설정 파일에 비워 둡니다. 암호화된 값이 이 필드에서 반환됩니다.

   다른 암호화 필드의 여러 **NameEncryptValuePair** 값을 추가할 수 있습니다.

   >[!NOTE]
   >
   >비어 있는 값 필드가 모두 제거됩니다.

1. *Server\*EncryptStrings** 폴더에 **EncryptedStrings.cfg** 파일을 저장합니다.

**출력 파일**

출력 파일이 &lt;*filename*>이 포함된 입력 파일과 동일한 이름으로 생성됩니다.*암호화된* 확장 프로그램. 예를 들어 입력 파일이 *sample.cfg* 로 지정되면 출력 파일이 *sample.cfg.encrypted*&#x200B;로 지정됩니다.
