---
description: Insight Server(InsightServer64.exe)를 사용하면 이벤트 데이터 또는 조회 데이터에서 사용자 지정 차원을 정의할 수 있습니다.
title: 확장 차원 정보
uuid: ae014a26-5286-4e36-9098-aaa463d9fe05
exl-id: f74aa85e-f880-4ab5-a8fb-128862aa808f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%

---

# 확장 차원 정보{#about-extended-dimensions}

{{eol}}

Insight Server(InsightServer64.exe)를 사용하면 이벤트 데이터 또는 조회 데이터에서 사용자 지정 차원을 정의할 수 있습니다.

정의하는 모든 사용자 지정 차원을 확장 차원이라고 합니다. 이를 사용하여 시각화를 만들거나, 확장 지표를 작성하거나, 분석을 수행하여 비즈니스 채널과 관련된 작업 및 문제를 이해할 수 있습니다. 에서 몇 가지 유형의 확장 차원을 정의할 수 있습니다 [!DNL Transformation.cfg] 파일 또는 위치 [!DNL Transformation Dataset Include] 파일.

확장 차원은 로그 필드 값과 상위 차원 간의 관계를 나타냅니다. 상위 차원은 모든 사용자 정의 가산 차원일 수 있습니다. 자세한 내용은 [가산 Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-count-dim.md#concept-f28b633419494e7bbc510012dbfcc6f8). 에서 차원을 정의할 때 상위를 지정합니다 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일. 차원의 상위 차원은 해당 수준과 동일합니다. 예를 들어 세션의 상위를 사용하여 차원을 정의하는 경우 해당 차원은 세션 수준 차원입니다.

>[!NOTE]
>
>로그 필드 값은 로그에서 사용할 수 있는 고유 값에서 가져올 수 있습니다( [!DNL .vsl]) 파일 또는 기타 이벤트 데이터 소스 또는 변환을 사용하여 생성된 확장 로그 필드에서 전송할 수 있습니다.

확장 차원을 시각화에 추가하려면 [!DNL Select Dimension] 메뉴 아래의 제품에서 사용할 수 있습니다. 예를 들어 그래프 시각화에 확장 차원을 추가하려면 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Visualization]** > **[!UICONTROL Graph]** > **[!UICONTROL Extended]** > *&lt;**[!UICONTROL dimension name]**>*. Data Workbench 인터페이스 내에서 확장 차원 목록을 구성하려는 경우 확장된 차원을 만든 하위 폴더로 이동할 수 있습니다. 의 관리 인터페이스 장을 참조하십시오. *Data Workbench 사용 안내서*. 이렇게 하면 시각화 추가 > 그래프 > 확장 > &lt; 과 같이 하위 폴더의 이름도 메뉴에 표시됩니다&#x200B;*하위 폴더 이름*> > &lt;*차원 이름*>.

데이터 세트 프로필에 대해 정의된 모든 차원과 각 차원에 대한 버퍼 크기를 보려면 [!DNL Detailed Status] data workbench 인터페이스 및 클릭 **[!UICONTROL Performance]**, 그런 다음 **[!UICONTROL Dimensions]** 노드를 확장하려면 다음을 수행하십시오. 쿼리 시간을 제어하는 버퍼 크기는 MB로 표시됩니다. 에 대한 자세한 정보 [!DNL Detailed Status] 인터페이스를 참조하십시오.
