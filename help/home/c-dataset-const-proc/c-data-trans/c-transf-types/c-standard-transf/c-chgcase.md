---
description: ChangeCase 변환은 Action 매개 변수에 지정된 대로 Input 매개 변수의 문자열 대/소문자를 변경합니다.
solution: Analytics
title: ChangeCase
topic: Data workbench
uuid: 676e79e6-324e-43d1-8982-b44596d0eeac
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# ChangeCase{#changecase}

ChangeCase 변환은 Action 매개 변수에 지정된 대로 Input 매개 변수의 문자열 대/소문자를 변경합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
|  이름  | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 작업 | 위 또는 아래 대/소문자를 위/아래로 변경할지 여부를 지정합니다. | lower |
| 설명 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 입력 | 입력으로 사용할 로그 항목의 필드 이름입니다. |  |
| 출력 | 출력 필드의 이름입니다. |  |

이 예에서는 웹 사이트 트래픽에서 수집된 데이터의 필드를 사용하며, s-dns 필드 내의 문자열 대/소문자가 소문자로 변경되고, 새 값은 새 필드인 x-소문자-dns에 출력됩니다.

![](assets/cfg_TransformationType_ChangeCase.png)

