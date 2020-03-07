---
description: 수식의 구문 규칙입니다.
solution: Analytics
title: 모든 식의 구문
topic: Data workbench
uuid: 663e3fd2-80e5-4805-8706-34a0e02ebd0f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 모든 식의 구문{#syntax-for-any-expression}

수식의 구문 규칙입니다.

* 공식에서 키워드는 대/소문자를 구분하므로 표시되는 그대로 정확히 입력해야 합니다.
* 공식에 공백이 포함된 지표, 차원 및 필터 이름은 단어 사이에 밑줄을 사용해야 합니다. 예: [!DNL Page_Views]
* 표현식 내의 문자열의 경우 특정 작은따옴표, 큰따옴표 및 백슬래시를 escape해야 합니다. 예:

   * [!DNL “can’t”] 는 허용되고 escape할 필요가 없지만, [!DNL ‘can’t’] 받아들일 수 없으며, 빠져나가야만 한다 [!DNL ‘can\’t’].

   * [!DNL c:\windows] 를 escape로 [!DNL c:\\windows]설정해야 합니다.

