---
description: 실험을 구성하기 전에 실험에 사용할 대체 콘텐츠를 만들어야 합니다.
solution: Analytics
title: 테스트 콘텐츠 만들기
uuid: d7996522-38a6-4bb8-9736-d71157c17b45
exl-id: fd46c6af-37e8-452a-880d-147b7d0cfe21
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 4%

---

# 테스트 콘텐츠 만들기{#creating-the-test-content}

{{eol}}

실험을 구성하기 전에 실험에 사용할 대체 콘텐츠를 만들어야 합니다.

컨트롤 그룹은 원래 URI로 전송되고 테스트 그룹은 새 대체 URI로 전송됩니다.

혼동을 방지하기 위해 테스트 그룹 파일 이름을 다시 사용하지 마십시오. 예를 들어 이름이 인 테스트 그룹 파일을 사용하여 실험을 실행하는 경우 [!DNL test2.asp]를 사용하지 않음 [!DNL test2.asp] 를 다음 실험에서 테스트 파일의 이름으로 사용합니다.

홈 페이지에서 &quot;데모 요청&quot; 그래픽 링크를 이동하는 것이 방문자 변환에 영향을 준다는 가설을 위해 새 위치에 &quot;데모 요청&quot; 그래픽 링크가 포함된 대체 홈 페이지를 만듭니다. 다음 섹션에서는 컨트롤 그룹 URI를 지정하는 방법에 대해 설명합니다 [!DNL index.asp] 테스트 그룹 URI로 대체됨 [!DNL index2.asp] 방문자의 일정 비율.
