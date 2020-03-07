---
description: Insight 서버(InsightServer64.exe)를 사용하면 이벤트 데이터 또는 조회 데이터에서 사용자 지정 차원을 정의할 수 있습니다.
solution: Analytics
title: 확장 치수 정보
topic: Data workbench
uuid: ae014a26-5286-4e36-9098-aaa463d9fe05
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 확장 치수 정보{#about-extended-dimensions}

Insight 서버(InsightServer64.exe)를 사용하면 이벤트 데이터 또는 조회 데이터에서 사용자 지정 차원을 정의할 수 있습니다.

정의한 사용자 정의 차원을 확장 차원이라고 합니다. 시각화를 만들거나 확장 지표를 만들거나 분석을 수행하여 비즈니스 채널과 관련된 작업 및 문제를 파악할 수 있습니다. 파일 또는 [!DNL Transformation.cfg] [!DNL Transformation Dataset Include] 파일에서 여러 유형의 확장 크기를 정의할 수 있습니다.

확장 차원은 로그 필드 값과 상위 차원 사이의 관계를 나타냅니다. 상위 차원은 모든 사용자 정의 계산 가능한 차원이 될 수 있습니다. 계산 [가능한 차원을 참조하십시오](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-count-dim.md#concept-f28b633419494e7bbc510012dbfcc6f8). 파일 또는 [!DNL Transformation.cfg] [!DNL Transformation Dataset Include] 파일에서 차원을 정의할 때 상위를 지정합니다. 차원의 상위는 해당 수준과 동일합니다. 예를 들어 세션의 상위로 차원을 정의하면 해당 차원은 세션 수준 차원입니다.

>[!NOTE]
>
>로그 필드 값은 로그( [!DNL .vsl]) 파일 또는 기타 이벤트 데이터 소스 또는 변형을 사용하여 만든 확장 로그 필드에서 사용할 수 있는 고유한 값에서 가져올 수 있습니다.

시각화에 확장 차원을 추가하려면 [!DNL Select Dimension] 메뉴 내의 확장 목록에서 액세스합니다. 예를 들어, 그래프 시각화에 확장 차원을 추가하려면 작업 영역 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Visualization]** > **[!UICONTROL Graph]** > **[!UICONTROL Extended]** > *&lt;**[!UICONTROL dimension name]**>*&#x200B;를 클릭합니다. 데이터 워크벤치 인터페이스 내에서 확장 차원 목록을 구성하려는 경우 확장 차원을 만든 하위 폴더로 이동할 수 있습니다. 데이터 워크벤치 사용 안내서의 관리 *인터페이스 장을 참조하십시오*. 이렇게 하면 시각화 추가 > 그래프 > 확장 > &lt;*하위 폴더 이름*> > &lt;*차원 이름*>에서와 같이 하위 폴더의 이름도 메뉴에 표시됩니다.

데이터 세트 프로필에 대해 정의된 모든 차원 및 각 데이터 세트에 대한 버퍼 크기를 보려면 데이터 워크벤치에서 [!DNL Detailed Status] 인터페이스를 열고 **[!UICONTROL Performance]**&#x200B;을 클릭한 다음 노드를 **[!UICONTROL Dimensions]** 확장합니다. 쿼리 시간을 제어하는 버퍼 크기는 MB 단위로 표시됩니다. 인터페이스에 대한 자세한 내용은 [!DNL Detailed Status] 서버 관리 및 설치 안내서를 참조하십시오.
