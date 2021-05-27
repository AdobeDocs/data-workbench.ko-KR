---
description: 문자열 및 숫자 매개 변수는 각각 해당 값 문자열 및 숫자로 가져옵니다.
title: 문자열 및 숫자 매개 변수
uuid: 2840967e-dd9e-40b2-91e4-3fdfa38f88e7
exl-id: 37d004da-cde7-4b67-b0cb-0acbb6d8ad68
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 5%

---

# 문자열 및 숫자 매개 변수{#string-and-numeric-parameters}

문자열 및 숫자 매개 변수는 각각 해당 값 문자열 및 숫자로 가져옵니다.

이러한 매개 변수를 서로 교환하여 사용할 수 있지만, 숫자 매개 변수는 숫자 값을 갖도록 정의해야 합니다. 변환, 조건 및 확장 차원을 정의할 때 문자열 및 숫자 매개 변수를 참조할 수 있으며 동일한 라인에서 두 개 이상의 매개 변수를 참조할 수 있습니다.

[!DNL Input] 또는 [!DNL Output] 필드에서 문자열 및 숫자 매개 변수를 참조할 수 없지만, 문자열 매개 변수를 사용하여 상수 입력 필드를 정의할 수 있습니다. 또한 디코더 또는 디코더 그룹에서 문자열 및 숫자 매개 변수를 참조할 수 없습니다.

이 예는 문자열 매개 변수와 숫자 매개 변수를 정의하는 [!DNL Log Processing Dataset Include] 파일을 보여줍니다. &quot;값 조회&quot;라는 문자열 매개 변수는 Data Workbench 서버 설치 디렉토리에 대한 파일 위치(조회\값)를 정의합니다.

![](assets/cfg_Parameters_StringNumeric.png)
