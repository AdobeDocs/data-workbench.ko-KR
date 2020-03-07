---
description: 복사 변환은 입력 필드의 값을 지정된 출력 필드에 복사하기만 하면 됩니다. 입력 필드가 문자열의 벡터일 수 있는 경우 출력 필드는 "x-"로 시작해야 합니다.
solution: Analytics
title: 복사
topic: Data workbench
uuid: 073f53bf-befb-4fba-a8f8-260ffcdd007c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 복사{#copy}

복사 변환은 입력 필드의 값을 지정된 출력 필드에 복사하기만 하면 됩니다. 입력 필드가 문자열의 벡터일 수 있는 경우 출력 필드는 &quot;x-&quot;로 시작해야 합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
|  이름  | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 설명 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건 테스트가 true이고 주어진 로그 항목에서 입력 값을 사용할 수 없는 경우에 사용됩니다. |  |
| 입력 | 복사할 필드의 이름입니다. |  |
| 출력 | 출력 필드의 이름입니다. |  |

이 예에서는 웹 사이트 트래픽에서 수집된 데이터 필드를 사용하는 출력 필드 x-purchase-success가 cs-uri가 일치할 때마다 &quot;1&quot;이라는 문자 값을 [!DNL /checkout/confirmed.php]받습니다. 값이 [!DNL Condition] [!DNL /checkout/confirmed.php]만족스럽지 않으면(즉, cs-uri-stem이 일치하지 않음) x-purchase-success가 변경되지 않습니다.

![](assets/cfg_TransformationType_Copy.png)

