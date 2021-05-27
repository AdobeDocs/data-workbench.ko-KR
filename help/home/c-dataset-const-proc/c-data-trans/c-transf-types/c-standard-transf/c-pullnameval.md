---
description: PullNameValues 변환은 cs-uri-query 필드의 값을 가져와서 각 이름-값 쌍을 별도의 문자열로 구분하는 특수 작업입니다.
title: 전체 이름 값
uuid: b24db987-78e8-4afc-9113-89aedc0170b2
exl-id: 3660ff6e-87dc-42cf-a897-0e2e0e021c07
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 4%

---

# 전체 이름 값{#pullnamevalues}

PullNameValues 변환은 cs-uri-query 필드의 값을 가져와서 각 이름-값 쌍을 별도의 문자열로 구분하는 특수 작업입니다.

이름-값 쌍 문자열의 전체 컬렉션은 지정된 출력 필드에 문자열의 벡터로 출력됩니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 댓글 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 주어진 로그 항목에서 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 출력 | 출력 문자열의 이름입니다. |  |

이 예제에서는 [!DNL PullNameValues] 변형을 사용하여 방문자의 검색 양식 사용을 캡처합니다.선택한 단추, 양식에 입력한 값 등 이 예제에서는 [!DNL String Match] 조건( [Conditions](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md) 참조)을 사용하여 이 변환의 사용을 [!DNL /search.php] 페이지에만 격리합니다. 이름-값 쌍의 벡터가 x-search-name 값으로 출력됩니다.

![](assets/cfg_TransformationType_PullNameValues.png)

위에서 정의한 대로 변형을 사용하면 cs-uri-stem 필드가 페이지 [!DNL /search.php] 및 cs-uri-query와 일치하면 다음과 같은 내용이 포함됩니다.

* Searchfor=Bob&amp;State=Virginia&amp;isMale=true

그런 다음 x-search-namvalue에는 다음 세 개의 문자열을 포함하는 벡터가 포함됩니다.

* Searchfor=Bob
* State=Virginia
* isMale=true
