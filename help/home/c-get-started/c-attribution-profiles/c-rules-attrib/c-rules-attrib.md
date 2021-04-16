---
description: Data Workbench에서 새로운 규칙 기반 속성 프로파일을 사용하여 속성 이벤트를 빠르게 분석하고 사용자가 정의한 성공적인 변환으로 이끄는 책임을 지정할 수 있습니다. 속성 프로필에는 데이터 아키텍트가 해당 기능을 설정하고 확장하는 데 필요한 정보가 포함되어 있으며 애널러가 바로 들어가서 분석할 수 있도록 미리 만들어진 작업 영역이 포함되어 있습니다.
title: 속성 프로필
uuid: 500e9e86-cffc-4f0d-a397-6521b493bf9a
exl-id: 29946f22-1d39-44ca-9474-13dbe228751c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# 속성 프로필{#attribution-profile}

Data Workbench에서 새로운 규칙 기반 속성 프로파일을 사용하여 속성 이벤트를 빠르게 분석하고 사용자가 정의한 성공적인 변환으로 이끄는 책임을 지정할 수 있습니다. 속성 프로필에는 데이터 아키텍트가 해당 기능을 설정하고 확장하는 데 필요한 정보가 포함되어 있으며 애널러가 바로 들어가서 분석할 수 있도록 미리 만들어진 작업 영역이 포함되어 있습니다.

기여도 프로필을 사용하면 마케팅 활동과 성공적인 고객 리드 생성 또는 판매 전환율 간의 관계에 대한 새로운 관점을 얻을 수 있습니다. 기여도 프로필은 고객 여정에서 실현된 매출 또는 기여도를 위해 크레딧의 할당을 받아야 하는 상호 작용을 평가하는 데 도움이 됩니다. 이를 통해 속성 이벤트를 신속하게 분석한 다음 성공적인 판매로 이어지는 첫 번째 또는 마지막 접촉 또는 다른 이벤트에 대한 책임을 할당할 수 있으므로 마케팅 활동 및 비용의 효과를 식별할 수 있습니다.

<!-- <a id="section_648A288E4CA84D579884BC161085C4D5"></a> -->

>[!IMPORTANT]
>
>속성 프로필은 분석(SC/Insight) 데이터 피드를 사용하는 Adobe SC 프로필을 구현한 사용자가 즉시 사용하도록 구성되어 있습니다. 기본적으로 마케팅 및 전환 이벤트는 제공된 규칙 기반 모델에서 평가되는 기본 상호 작용 유형으로 사용됩니다.

자세한 내용은 [속성 프로필 배포](../../../../home/c-get-started/c-attribution-profiles/c-rules-attrib/c-attrib-profile-deploy.md#concept-fbcb5800cd6a40cc901e61f3882988c0) 및 [속성 모델](../../../../home/c-get-started/c-attribution-profiles/c-rules-attrib/c-attrib-models.md#concept-e209c7e86a5c4008ad6d78fdf4ea032d)을 참조하십시오.

## 아키텍처 및 애널리스트 작업 영역 {#section-27c6aff70ba147cca6e11451e127afb4}

속성 프로필 내에 워크벤치의 별도의 탭에 설계자 및 애널리스트 작업 영역이 정의되어 있습니다.

![](assets/attribution_profile_tabs.png)

**아키텍처 작업 영역**

**속성** 탭에서 **[!UICONTROL Architect Workspace]** 탭을 클릭하여 기본 속성 모델링을 위해 구성 파일을 설정하기 위해 특별히 디자인된 작업 영역을 엽니다.

![](assets/attribution_profile_arch.png)

아키텍처 탭에는 프로필 데이터 집합 폴더의 각 구성 파일을 단계별로 안내하는 작업 영역이 포함되어 있습니다. 예를 들어 **[!UICONTROL Attribution Configuration - Step 1]**&#x200B;에서는 [!DNL profile.cfg] 파일의 [변형] 섹션 내에서 속성 값을 식별할 수 있습니다.

![](assets/attribution_profile_arch_step1.png)

**애널리스트** 작업  **[!UICONTROL Analyst]** **[!UICONTROL Workspaces]** 영역 탭을 클릭하여 속성 프로필과 함께 제공되는 차원 및 지표를 활용하여 미리 작성된 작업 영역 분석을 엽니다.

이러한 작업 영역은 다음 4가지 범주로 구성됩니다.

1. **기본** 보고작업 공간 내에서 단일 모델을 포즈합니다.
1. **비교** 보고서에서는 단일 뷰 내에 여러 모델을 표시하여 분석을 확장했습니다.
1. **조사 보고서** 는 보고 템플릿을 확장하여 다양한 형식으로 속성 모델을 표시합니다. 또한 이 섹션에서는 위치 기반 가중치를 소개하고 표시합니다.
1. **경로** 지정 보고서프로세스 흐름 및 상호 작용 경로를 완전히 탐색 및 표현하기 위해 여러 경로 지정 시각화를 사용하여 고객의 마케팅 여정을 표시합니다.

![](assets/attribution_profile_analyst.png)

애널리스트 탭에는 보고서와 함께 미리 구성된 작업 영역이 포함되어 있습니다. 예를 들어 **[!UICONTROL First Attribution]**&#x200B;에서는 **[!UICONTROL Campaign]** 테이블에서 **[!UICONTROL Time]**&#x200B;에 기반한 **[!UICONTROL Revenue]** 속성을 볼 수 있습니다.

![](assets/attribution_profile_analyst_step1.png)
