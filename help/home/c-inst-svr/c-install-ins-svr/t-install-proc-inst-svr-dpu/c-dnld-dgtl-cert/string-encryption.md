---
description: 클라이언트와 서버 간의 통신 시 암호 및 기타 문자열을 암호화합니다.
title: 문자열 암호화
uuid: b2ec6a10-136c-4694-a425-04dbb41d43d1
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 문자열 암호화{#string-encryption}

클라이언트와 서버 간의 통신 시 암호 및 기타 문자열을 암호화합니다.

데이터 워크벤치 클라이언트(워크스테이션)와 서버 간에 통신할 때 Value 매개 변수(암호 등)를 EncryptedString 유형으로 저장할 수 *있습니다*. 그러면 매개 변수가 숨겨지고 해당 키가 반환된 *상태로* 서버의 Windows 자격 증명 저장소에 문자열이 저장됩니다. 기본적으로 내보내기에 사용되는 자격 증명이 저장되지만 매개 변수를 암호화하는 데 사용할 수 있습니다.

* Server\*EncryptStrings*에 새&#x200B;*폴더가 추가되었습니다*.

   구성 파일을 설정하여 문자열을 암호화합니다.

* Server\Component\*EncryptedStrings.cfg **에 새 구성 파일이 추가되었습니다*.

   ```
   component = EncryptionComponent:
     Path = Path: EncryptStrings\\*.cfg
   ```

   이 파일은 암호화 구성 *파일을*&#x200B;위해 Server\*EncryptStrings* 폴더를 폴링합니다.

**문자열을**&#x200B;암호화하려면

1. 다음 **필드를** 설정하여 문자열에 대한 EncryptedStrings.cfg 구성 파일을 만듭니다.

   ```
   Names = vector: 1 items
    0 = NameEncryptValuePair:
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server
     Name = string: // Name for identifier 
     Value = string: // Value to be encrypted
   ```

   * *값* - 이 필드에는 암호화해야 하는 일반 텍스트 문자열이 포함되어 있습니다.

      서버 측 암호입니다. 값 *설정은* 서버 컴퓨터에서만 암호화됩니다.

   * *이름* - 이 필드에는 암호화된 문자열을 식별하는 값이 포함되어 있습니다.
   * *EncryptValue* - 이 필드는 입력 구성 파일에 비어 있게 됩니다. 암호화된 값이 이 필드에 반환됩니다.
   암호화에 대해 여러 **필드에** NameEncryptValuePair 값을 추가할 수 있습니다.

   >[!NOTE]
   >
   >빈 값 필드는 모두 제거됩니다.

1. EncryptedStrings. **cfg** 파일을 Server\*EncryptStrings ** 폴더에*&#x200B;저장합니다.

**출력 파일**

출력 파일은 &lt;*filename*>의 입력 파일과 동일한 이름으로 생성됩니다.*암호화된* 확장. 예를 들어 입력 파일의 이름이 *sample.cfg* 인 경우 출력 파일의 이름은 *sample.cfg.encrypted*&#x200B;입니다.
