---
description: 실험을 구성하려면 먼저 실험에서 사용할 대체 컨텐츠를 만들어야 합니다.
solution: Analytics,Analytics
title: 테스트 콘텐츠 만들기
uuid: d7996522-38a6-4bb8-9736-d71157c17b45
exl-id: fd46c6af-37e8-452a-880d-147b7d0cfe21
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 4%

---

# 테스트 콘텐츠 만들기{#creating-the-test-content}

실험을 구성하려면 먼저 실험에서 사용할 대체 컨텐츠를 만들어야 합니다.

제어 그룹은 원래 URI로 전송되고 테스트 그룹은 새 대체 URI로 전송됩니다.

혼동을 방지하려면 테스트 그룹 파일 이름을 다시 사용하지 마십시오. 예를 들어 [!DNL test2.asp] 테스트 그룹 파일을 사용하여 실험을 실행하는 경우 다음 실험에서 테스트 파일의 이름으로 [!DNL test2.asp]을 사용하지 마십시오.

홈 페이지에서 &quot;데모 요청&quot; 그래픽 링크를 이동하는 것이 방문자 전환에 영향을 준다는 가설을 위해 Adobe는 새 위치의 &quot;데모 요청&quot; 그래픽 링크가 포함된 대체 홈 페이지를 만듭니다. 다음 섹션에서는 특정 비율의 방문자에 대해 제어 그룹 URI [!DNL index.asp]을 테스트 그룹 URI [!DNL index2.asp]으로 대체하도록 지정하는 방법을 설명합니다.
