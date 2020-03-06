---
description: 실험을 배포한 후 테스트가 제대로 작동하는지 확인해야 합니다.
solution: Insight,Analytics
title: 실험 검증
topic: Data workbench
uuid: 59769f5b-4175-479e-ad7d-7226e9c666af
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 실험 검증{#validating-the-experiment}

실험을 배포한 후 테스트가 제대로 작동하는지 확인해야 합니다.

ExpCookieURL [매개 변수 수정(선택 사항)](../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expckurl-prm.md#concept-215bf86bab4e4ec0b0cc803ec48a8fcf)에서 설명한 바와 같이 [!DNL Sensor] 구성 파일의 ExpCookieURL 매개 변수에 지정된 페이지를 사용하여 특정 실험 그룹에 자신을 배치할 수 있습니다.

기본 가상 페이지는 [!DNL /setcookie.htm]으로 설정되지만 ExpCookieURL 매개 변수에서 설정한 값을 사용해야 합니다.

## 테스트 페이지 요청 {#section-8aed3b48d47f4e6c8869c0216f8781b1}

웹 사이트에 대한 특정 실험 그룹을 테스트하려면 브라우저가 쿠키를 승인하도록 구성되어야 하며 이 웹 사이트에 대한 쿠키가 아직 없어야 합니다.

새 그룹을 테스트할 때마다 웹 사이트의 쿠키를 지워야 합니다.

특정 실험 내의 특정 그룹에 자신을 포함하려면 다음 형식으로 쿼리 문자열이 있는 테스트 페이지를 요청합니다.

[!DNL http://] *&lt;[!DNL sitename/?Experiment Name=Group Name]>*

예:

[!DNL http://www.omniture.com/setcookie.htm?New_Homepage=index2]

가상 URL 요청이 서버로 전송되면 [!DNL Sensor] 지정된 실험 내에서 지정된 그룹의 구성원으로 식별된 다음 웹 사이트의 루트로 리디렉션합니다. 이제 웹 사이트의 적절한 위치로 이동하여 해당 실험 및 그룹에 대한 올바른 컨텐츠가 표시되는지 확인할 수 있습니다.

브라우저에 다음을 입력하면 브라우저가 웹 사이트의 홈 페이지를 표시하고 New_Homepage 실험 내에서 index2 그룹에 배치하게 됩니다.

[!DNL http://www.omniture.com/setcookie.htm?New_Homepage=index2]

index2 그룹의 방문자가 홈 페이지를 요청하면 다음 그래픽과 같이 &quot;데모 요청&quot; 그래픽 링크가 페이지 위에 표시됩니다.

![](assets/TestPage.png)

