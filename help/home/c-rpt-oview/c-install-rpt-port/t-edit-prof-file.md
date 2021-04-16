---
description: 보고서 포털에서 사용할 수 있게 하려는 프로필을 지정하려면 profiles.xml 파일을 구성해야 합니다.
title: Profiles.xml 파일 편집
uuid: 3640552b-bc46-4b4f-8524-e021b0ca2bfc
exl-id: 7a3900e4-e472-4295-80f7-ce755958bc18
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# Profiles.xml 파일 편집{#edit-the-profiles-xml-file}

보고서 포털에서 사용할 수 있게 하려는 프로필을 지정하려면 profiles.xml 파일을 구성해야 합니다.

[!DNL profiles.xml] 파일은 출력용으로 지정한 폴더에 있습니다. 기본적으로 \*PortalName*\PortalFiles\Output folder폴더에 있습니다.

**profiles.xml 파일에 프로필 이름을 추가하려면**

1. IIS가 실행 중인 컴퓨터에서 메모장과 같은 텍스트 편집기에서 [!DNL profiles.xml] 파일을 엽니다.
1. 다음 예제와 같이 포털에서 각 [!DNL Profile]에 대한 프로필 요소 및 태그를 추가합니다.

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
