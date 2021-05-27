---
description: ChangeCase 변환은 Action 매개 변수에 지정된 대로 Input 매개 변수에서 문자열의 대/소문자를 변경합니다.
title: 대소문자 변경
uuid: 676e79e6-324e-43d1-8982-b44596d0eeac
exl-id: 2002fe22-d31c-4286-9f73-59ef205f1384
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 8%

---

# 대소문자 변경{#changecase}

ChangeCase 변환은 Action 매개 변수에 지정된 대로 Input 매개 변수에서 문자열의 대/소문자를 변경합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 작업 | 위쪽 또는 아래쪽. 대/소문자를 위/아래로 변경할지 여부를 지정합니다. | lower |
| 댓글 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 입력 | 입력으로 사용할 로그 항목의 필드 이름입니다. |  |
| 출력 | 출력 필드의 이름입니다. |  |

웹 사이트 트래픽에서 수집된 데이터의 필드를 사용하는 이 예에서 s-dns 필드 내의 문자열 대/소문자가 소문자로 변경되고 새 값이 새 필드인 x-lowercase-dns에 출력됩니다.

![](assets/cfg_TransformationType_ChangeCase.png)
