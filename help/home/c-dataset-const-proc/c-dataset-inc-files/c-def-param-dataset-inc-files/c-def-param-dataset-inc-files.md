---
description: 데이터 세트를 구성할 때 매개 변수인 변수를 정의하여 의미 있는 값을 표현할 수 있습니다.
title: 데이터 세트에 있는 매개 변수 정의 포함 파일
uuid: 1eb7d48c-a107-4b32-abca-55d30586813f
exl-id: 80bb77e1-a157-4e16-9519-6d0e2ce17fe1
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 3%

---

# 데이터 세트에 있는 매개 변수 정의 포함 파일{#defining-parameters-in-dataset-include-files}

데이터 세트를 구성할 때 매개 변수인 변수를 정의하여 의미 있는 값을 표현할 수 있습니다.

매개 변수(매개 변수 정의)에 값을 할당하려면 로그 처리 또는 [!DNL Transformation Dataset Include] 파일의 매개 변수 벡터에 매개 변수의 이름과 값을 추가합니다. 매개 변수를 정의한 후에는 데이터 세트 프로필의 구성 파일에서 매개 변수를 참조할 수 있습니다. 이러한 매개 변수를 정의하고 참조하는 것을 매개 변수 대체라고 합니다. 데이터 세트를 구성할 때 매개 변수 대체를 사용하면 매개 변수 정의에 대한 중앙 위치를 만들 수 있습니다. 여러 번 또는 여러 파일에서 참조되는 매개 변수를 업데이트해야 하는 경우 한 번만 변경하면 됩니다.

>[!NOTE]
>
>이 안내서에서는 용어 매개 변수를 사용하여 구성 파일의 설정 이름(예: 로그 항목 조건, 재처리 또는 변형)을 참조합니다. 그러나 이 단원에서 사용되는 매개 변수는 구성 파일의 설정 이름이 아니라 데이터세트에 있는 매개 변수 벡터의 구성원을 특히 참조합니다.

매개 변수를 정의할 때는 다음 점을 고려해야 합니다.

* 매개 변수는 정확하게 한 번만 정의해야 합니다. 따라서 여러 데이터 세트에 파일이 포함된 같은 변수를 정의할 수 없습니다.
* 정의하는 모든 매개 변수는 로그 처리 또는 변형 단계에 로컬이지만 해당 단계에 대해 여러 데이터 세트 구성 파일에 걸쳐 전역적입니다. 예를 들어 [!DNL Transformation Dataset Include] 파일에서 매개 변수를 정의하면 매개 변수가 전체 변형 단계에 대해 정의되고 상속된 프로파일에 대한 [!DNL Transformation.cfg] 파일과 다른 모든 [!DNL Transformation Dataset Include] 파일에서 참조할 수 있습니다. 로그 처리를 위해 매개 변수를 정의하지 않았습니다.따라서 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 파일의 매개 변수에 대한 모든 참조는 처리 오류를 생성합니다.

**매개 변수를 정의하려면**

[!DNL Log Processing] 및 [!DNL Transformation Include] 파일에서 문자열, 숫자 및 벡터 매개 변수를 정의할 수 있습니다.

1. [!DNL Log Processing] 또는 [!DNL Transformation Dataset Include] 파일의 데이터 워크벤치 창에서 **[!UICONTROL Parameters]**&#x200B;를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL Parameter]**&#x200B;를 클릭합니다.

1. **[!UICONTROL String Parameter]**, **[!UICONTROL Numeric Parameter]** 또는 **[!UICONTROL Vector Parameter]**&#x200B;를 선택하고 다음 섹션에 설명된 대로 이름 및 값 매개 변수를 완료합니다.

1. 매개 변수를 정의한 파일이 데이터 세트에 포함되어 있는 파일을 저장하려면 창 맨 위에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 [!DNL User] 열의 파일 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;를 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 데이터 세트 포함 파일이 속한 상속된 프로필입니다.

>[!NOTE]
>
>이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰여지기 때문에 수정된 구성 파일을 Adobe에서 제공하는 내부 프로파일에 저장하지 마십시오.

**매개 변수를 참조하려면**

* 다른 데이터 집합 구성 파일에서 정의된 매개 변수를 참조하려면 해당 이름을 [!DNL $(parameter name)]으로 입력해야 합니다.

다음 섹션에서는 정의할 수 있는 매개 변수의 유형을 설명합니다.

* [문자열 및 숫자 매개 변수](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-string-num-param.md#concept-14f391ce107c4a3dad827ec7967f1080)
* [벡터 매개 변수](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-vector-param.md#concept-adb42a5474e245a9996d0aa8d5d522d0)
