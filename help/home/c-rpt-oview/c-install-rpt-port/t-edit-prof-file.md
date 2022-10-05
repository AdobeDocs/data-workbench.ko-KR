---
description: 보고서 포털에서 사용할 수 있는 프로필을 지정하려면 profiles.xml 파일을 구성해야 합니다.
title: Profiles.xml 파일 편집
uuid: 3640552b-bc46-4b4f-8524-e021b0ca2bfc
exl-id: 7a3900e4-e472-4295-80f7-ce755958bc18
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# Profiles.xml 파일 편집{#edit-the-profiles-xml-file}

{{eol}}

보고서 포털에서 사용할 수 있는 프로필을 지정하려면 profiles.xml 파일을 구성해야 합니다.

다음 [!DNL profiles.xml] 파일은 출력을 위해 지정한 폴더에 있습니다. 기본적으로 \*PortalName*\PortalFiles\Output 폴더에 있습니다.

**profiles.xml 파일에 프로필 이름을 추가하려면**

1. IIS가 실행 중인 컴퓨터에서 [!DNL profiles.xml] 메모장과 같은 텍스트 편집기에 있는 파일입니다.
1. 각각에 대해 프로필 요소와 태그를 추가합니다 [!DNL Profile] 포털에서 다음 예와 같이,

   ```
   <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <PROFILES>
     <PROFILE>
       <NAME>Product Sales</NAME>
     </PROFILE>
     <PROFILE>
       <NAME>Product Marketing</NAME>
     </PROFILE>
   </PROFILES>
   ```

1. 파일을 저장하고 닫습니다.
