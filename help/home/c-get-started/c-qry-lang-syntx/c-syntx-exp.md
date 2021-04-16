---
description: 수식의 구문 규칙입니다.
title: 모든 표현식의 구문
uuid: 663e3fd2-80e5-4805-8706-34a0e02ebd0f
exl-id: ca1a52c1-b5bd-48bd-95cd-f8059913bd0a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 13%

---

# 모든 표현식의 구문{#syntax-for-any-expression}

수식의 구문 규칙입니다.

* 수식에서 키워드는 대/소문자를 구분하며 표시되는 대로 정확하게 입력해야 합니다.
* 공식에 공백이 포함된 지표, 차원 및 필터 이름은 단어 사이에 밑줄을 사용해야 합니다. 예: [!DNL Page_Views]
* 표현식 내의 문자열의 경우 특정 작은따옴표, 큰따옴표 및 백슬래시를 escape해야 합니다. 예를 들어,

   * [!DNL “can’t”] 는 허용 가능하고 이스케이프할 필요가 없지만,  [!DNL ‘can’t’] 받아들일 수 없으며, 빠져나가야 합니다 [!DNL ‘can\’t’].

   * [!DNL c:\windows] 를 escape해야 합니다 [!DNL c:\\windows].
