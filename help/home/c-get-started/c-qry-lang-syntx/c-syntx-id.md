---
description: 지표, 차원 및 필터 표현식은 지정된 지표, 차원 및 필터를 참조하기 위해 식별자를 사용할 수 있습니다.
solution: Analytics
title: 식별자용 구문
topic: Data workbench
uuid: 9cfa188a-05ca-4163-a268-e33fce9a1929
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 식별자용 구문{#syntax-for-identifiers}

지표, 차원 및 필터 표현식은 지정된 지표, 차원 및 필터를 참조하기 위해 식별자를 사용할 수 있습니다.

이러한 식별자는 대/소문자를 구분하며 정의된 대로 정확히 입력해야 합니다.

유효한 식별자는 다음 중 하나 이상을 포함할 수 있습니다.

* 밑줄(_). 식별자의 밑줄은 지표, 차원 또는 필터 이름의 공백을 나타냅니다. 예를 들어 세션 레퍼러 차원은 표현식으로 [!DNL Session_Referrer] 언급됩니다.
* 백분율 기호(%)
* 대문자(A-Z)
* 소문자(a-z)
* 달러 기호($)
* 식별자의 첫 번째 문자를 제외한 숫자(0-9).
* 비ASCII 문자

식별자는 다른 모든 문자를 사용할 수 없습니다.

이러한 동일한 규칙이 지표, 차원 및 필터 이름이 표현식 밖에서 사용될 때 이름에 공백을 포함할 수 있지만 밑줄은 사용할 수 없습니다. 예를 들어, [!DNL Transformation.cfg] 파일에서 세션 레퍼러 차원을 세션 레퍼러로 정의할 수는 있지만, 정의할 수는 없습니다 [!DNL Session_Referrer].
