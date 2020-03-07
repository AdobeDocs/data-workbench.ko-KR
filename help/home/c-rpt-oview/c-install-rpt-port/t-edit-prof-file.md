---
description: 보고서 포털에서 사용할 프로필을 지정하려면 profiles.xml 파일을 구성해야 합니다.
solution: Analytics
title: Profiles.xml 파일 편집
topic: Data workbench
uuid: 3640552b-bc46-4b4f-8524-e021b0ca2bfc
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Profiles.xml 파일 편집{#edit-the-profiles-xml-file}

보고서 포털에서 사용할 프로필을 지정하려면 profiles.xml 파일을 구성해야 합니다.

이 [!DNL profiles.xml] 파일은 출력을 위해 지정한 폴더에 있습니다. 기본적으로 PortalName*\PortalFiles\Output folder폴더에 있습니다.

**profiles.xml 파일에 프로필 이름을 추가하려면**

1. IIS가 실행 중인 컴퓨터에서 메모장과 같은 텍스트 편집기에서 [!DNL profiles.xml] 파일을 엽니다.
1. 다음 예와 같이 포털에서 각 [!DNL Profile] 항목에 대한 프로필 요소 및 태그를 추가합니다.

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
