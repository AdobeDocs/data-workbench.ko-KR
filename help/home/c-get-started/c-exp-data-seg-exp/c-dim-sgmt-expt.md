---
description: 내보내려는 모든 데이터는 프로필 내의 차원으로 정의해야 합니다.
title: 세그먼트 내보내기에 사용할 차원 만들기
uuid: 7fdc043e-b2c5-4eac-adf4-bf60df6a3953
exl-id: 0f16c242-10f6-4014-b848-ea001e9d085c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 8%

---

# 세그먼트 내보내기에 사용할 차원 만들기{#create-dimensions-for-use-with-segment-export}

내보내려는 모든 데이터는 프로필 내의 차원으로 정의해야 합니다.

해당 차원이 프로파일에 아직 존재하지 않으면 해당 차원을 생성해야 합니다. 다음 방법 중 하나를 사용하여 차원을 만들 수 있습니다.

* [!DNL Transformation.cfg] 파일에 차원을 추가합니다. *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

* 새 [!DNL .dim] 파일을 만듭니다. [파생된 Dimension 만들기 및 편집](../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-dvrd-dim.md#concept-ece3c3ea8cdf4fc796680173993bff93)을 참조하십시오.

* 프로세스 맵이나 세그먼트와 같은 시각화에서 선택하고 선택 항목을 차원으로 저장합니다. [프로세스 맵에서 Dimension 저장](../../../home/c-get-started/c-analysis-vis/c-proc-maps/t-dim-proc-maps.md#task-44d9e555d4a944e6aa81993eef703051) 및 [세그먼트 Dimension 만들기](../../../home/c-get-started/c-analysis-vis/c-seg/c-create-seg-dim.md#concept-70b363edcad14185ba8051646ad3d44e)를 참조하십시오.

추적 ID 또는 이메일 주소(많은 요소가 있을 수 있음)와 같은 데이터 필드를 내보내려면 데이터의 원시 문자열을 저장하는 비정상 차원을 만들어야 합니다.

비정상 차원에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.
