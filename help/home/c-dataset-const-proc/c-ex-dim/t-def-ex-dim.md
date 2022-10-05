---
description: 확장 차원을 정의하는 단계입니다.
title: 확장 차원 정의
uuid: 25946998-54ca-4595-a2f9-9c593917643a
exl-id: e1664548-e2b4-47bb-8bec-155c16873e08
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 9%

---

# 확장 차원 정의{#defining-extended-dimensions}

{{eol}}

확장 차원을 정의하는 단계입니다.

1. 데이터 세트 프로필에서 작업하는 동안 [!DNL Profile Manager] 을(를) 클릭합니다. **[!UICONTROL Dataset]** 콘텐츠를 표시합니다.
1. 를 엽니다. [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 확장 차원을 정의할 파일입니다.

   * (권장) 데이터 집합에 포함된 파일을 열려면 다음을 참조하십시오 [데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

      >[!NOTE]
      >
      >Adobe은 하나 이상의 새 버전에서 확장 차원을 정의하는 것을 권장합니다 [!DNL Transformation Dataset Include] 파일. 자세한 내용은 [새 데이터 집합 만들기 포함 파일](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e).

   * 를 열려면 [!DNL Transformation.cfg] 파일, [변형 구성 파일 편집](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc).

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Transformations]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > *&lt;**[!UICONTROL Extended dimension type]**>*.
1. 확장 차원에 대한 적절한 정보를 입력합니다. 변형 유형에 대한 설명 및 해당 매개 변수에 대한 정보는 다음 섹션을 참조하십시오.

   * [가산 차원](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-count-dim.md#concept-f28b633419494e7bbc510012dbfcc6f8)
   * [단순 차원](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-simple-dim.md#concept-c1d804dac4094489afe61560d2908181)
   * [다대다 차원](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-many-dim.md#concept-5ed3cca8b2194d4f96134f6238040998)
   * [숫자 차원](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-num-dim.md#concept-8513b9afaff447c8b334410b565b91ed)
   * [비정상 차원](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-denormal-dim.md#concept-54a2600b8ee748b7acff405daccf3489)
   * [시간 차원](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-time-dim.md#concept-1e4eeb8d33964bb2a8d5768d6439df67)

      정의한 확장 차원에 대해 설명 매개 변수에 하나 이상의 주석 라인을 추가하여 차원을 추가로 설명하거나 해당 용도에 대한 메모를 추가할 수 있습니다. 주석을 추가하려면 **[!UICONTROL Comments]** 레이블을 지정하고 **[!UICONTROL Add new]** > **[!UICONTROL Comment Line]**.

1. 구성 파일에서 확장 차원을 정의했으면 파일을 로컬로 저장하고 Data Workbench 서버의 데이터 세트 프로필에 저장합니다.
