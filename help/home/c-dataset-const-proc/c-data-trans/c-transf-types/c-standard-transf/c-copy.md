---
description: 복사 변환은 입력 필드의 값을 지정된 출력 필드에 복사하는 것입니다. 입력 필드가 문자열 벡터일 수 있는 경우 출력 필드는 "x-"로 시작해야 합니다.
title: 복사
uuid: 073f53bf-befb-4fba-a8f8-260ffcdd007c
exl-id: 04e97006-1e8e-4123-bbbc-b90a5231170f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 6%

---

# 복사{#copy}

복사 변환은 입력 필드의 값을 지정된 출력 필드에 복사하는 것입니다. 입력 필드가 문자열 벡터일 수 있는 경우 출력 필드는 &quot;x-&quot;로 시작해야 합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 댓글 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건 테스트가 true이고 입력 값을 주어진 로그 항목에서 사용할 수 없는 경우에 사용됩니다. |  |
| 입력 | 복사할 필드의 이름입니다. |  |
| 출력 | 출력 필드의 이름입니다. |  |

이 예에서는 웹 사이트 트래픽에서 수집된 데이터의 필드를 사용하는 경우, cs-uri-stem이 [!DNL /checkout/confirmed.php]과 일치할 때마다 출력 필드 x-purchase-success는 &quot;1&quot;이라는 문자 값이 제공됩니다. [!DNL Condition]이 충족되지 않으면(즉, cs-uri-stem이 [!DNL /checkout/confirmed.php]과 일치하지 않으면 x-purchase-success가 변경되지 않습니다.

![](assets/cfg_TransformationType_Copy.png)
