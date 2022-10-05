---
description: 수식의 구문 규칙.
title: 모든 표현식의 구문
uuid: 663e3fd2-80e5-4805-8706-34a0e02ebd0f
exl-id: ca1a52c1-b5bd-48bd-95cd-f8059913bd0a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 13%

---

# 모든 표현식의 구문{#syntax-for-any-expression}

{{eol}}

수식의 구문 규칙.

* 수식에서 키워드는 대/소문자를 구분하므로 나타나는 대로 정확히 입력해야 합니다.
* 수식에서 공백을 포함하는 지표, 차원 및 필터 이름은 단어 사이에 밑줄을 사용해야 합니다. 예: [!DNL Page_Views]
* 표현식 내의 문자열의 경우 특정 작은따옴표, 큰따옴표 및 백슬래시를 이스케이프 처리해야 합니다. 예:

   * [!DNL “can’t”] 은(는) 사용할 수 있으며 이스케이프 처리할 필요가 없습니다. [!DNL ‘can’t’] 는 허용되지 않으며 [!DNL ‘can\’t’].

   * [!DNL c:\windows] 는 [!DNL c:\\windows].
