---
description: 실험을 구성하려면 먼저 실험에서 사용할 대체 컨텐츠를 만들어야 합니다.
solution: Insight,Analytics
title: 테스트 컨텐츠 만들기
topic: Data workbench
uuid: d7996522-38a6-4bb8-9736-d71157c17b45
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 테스트 컨텐츠 만들기{#creating-the-test-content}

실험을 구성하려면 먼저 실험에서 사용할 대체 컨텐츠를 만들어야 합니다.

제어 그룹은 원래 URI로 전송되고 테스트 그룹은 새 대체 URI로 전송됩니다.

혼동을 방지하려면 테스트 그룹 파일 이름을 재사용하지 마십시오. 예를 들어 이름이 [!DNL test2.asp]지정된 테스트 그룹 파일을 사용하여 실험을 실행하는 경우 다음 실험에서 테스트 파일의 [!DNL test2.asp] 이름으로 사용하지 마십시오.

홈 페이지에서 &quot;데모 요청&quot; 그래픽 링크를 이동하는 것이 방문자 전환에 영향을 준다는 가설을 위해 새 위치의 &quot;데모 요청&quot; 그래픽 링크가 포함된 대체 홈 페이지를 만듭니다. 다음 섹션에서는 특정 비율의 방문자에 대해 제어 그룹 URI를 테스트 그룹 URI로 [!DNL index.asp] 대체하도록 지정하는 방법을 설명합니다 [!DNL index2.asp] .
