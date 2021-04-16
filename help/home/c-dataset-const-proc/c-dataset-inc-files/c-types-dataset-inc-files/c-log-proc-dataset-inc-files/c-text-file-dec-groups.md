---
description: 로그 원본으로 로그 파일을 처리하려면 로그 처리 데이터 집합 포함 파일 내의 디코더에 대한 정의가 있어야 로그 항목에서 데이터 필드를 추출할 수 있습니다.
title: 텍스트 파일 디코더 그룹
uuid: 3ff9700b-4f34-4098-8827-6856897bdb28
exl-id: e9f6e02e-7150-455f-96f0-f34d98cc31b7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# 텍스트 파일 디코더 그룹{#text-file-decoder-groups}

로그 원본으로 로그 파일을 처리하려면 로그 처리 데이터 집합 포함 파일 내의 디코더에 대한 정의가 있어야 로그 항목에서 데이터 필드를 추출할 수 있습니다.

로그 파일 로그 소스에 대한 텍스트 파일 디코더 그룹을 정의하려면 로그 파일의 구조 및 내용, 추출할 데이터 및 해당 데이터가 저장되는 필드에 대한 지식이 필요합니다. 이 섹션에서는 디코더에 대해 지정할 수 있는 매개 변수에 대한 기본적인 설명을 제공하지만 디코더를 사용하는 방법은 소스 데이터가 포함된 로그 파일에 따라 달라집니다.

로그 파일 로그 소스의 형식 요구 사항에 대한 자세한 내용은 [로그 파일](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)을 참조하십시오. 텍스트 파일 디코더 정의에 대한 도움이 필요하면 Adobe에 문의하십시오.

텍스트 파일 디코더 그룹은 다음을 포함할 수 있습니다.

* [정규 표현식 디코더](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#section-67aca2c1f008404da7f845a64abec97c)
* [구분된 디코더](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#section-7e0a23decdbc4c75ae750a42446997a6)

## 정규 표현식 디코더 {#section-67aca2c1f008404da7f845a64abec97c}

일반 표현식 디코더는 로그 파일의 로그 항목 내에서 복잡한 문자열 패턴을 식별하고 이러한 패턴을 데이터 필드로 추출합니다. 각 디코더의 경우 필드 수는 일반 표현식의 캡처 하위 패턴 수와 같아야 합니다. 하위 패턴을 캡처하는 n번째 패턴과 일치하는 라인의 부분은 해당 라인의 n번째 필드에 지정됩니다.

**텍스트 파일 디코더 그룹에 정규 표현식 디코더를 추가하려면**

1. [기존 데이터 세트 포함 파일 편집](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077)에 설명된 대로 [!DNL Log Processing Dataset Include] 파일을 열고 텍스트 파일 디코더 그룹을 추가합니다. 테이블 항목 [디코더 그룹](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab)을 참조하십시오.

1. 새로 만든 디코더 그룹 아래의 **[!UICONTROL Decoders]**&#x200B;을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL Regular Expression]**&#x200B;를 클릭합니다.

1. 다음 정보를 지정합니다.

   * **필드:** 로그 파일의 필드 목록입니다. 여기에 정의된 필드를 데이터 세트 구성의 변형 단계로 전달하려면 해당 필드가 데이터 세트에 대한 [!DNL Log Processing Dataset Include] 파일 중 하나의 필드 매개 변수에 나열되어야 합니다. 사용자 정의 필드 이름은 &quot;x-&quot;로 시작해야 합니다.

   * **이름:** 디코더의 선택적 식별자입니다.
   * **정규 표현식:** 파일의 각 행에서 원하는 필드를 추출하는 데 사용됩니다.

1. 그룹에 추가하려는 다른 디코더에 대해 4단계와 5단계를 반복합니다.
1. [!DNL Log Processing Dataset Include] 파일을 저장하려면 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;를 클릭합니다.

1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 [!DNL User] 열에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. 프로필 이름은 데이터 집합 프로필의 이름이거나 데이터 집합 포함 파일이 속하는 상속된 프로필입니다.**[!UICONTROL Save to]*****[!UICONTROL profile name]***

이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰여지기 때문에 수정된 구성 파일을 Adobe에서 제공하는 내부 프로파일에 저장하지 마십시오.

>[!NOTE]
>
>주어진 로그 파일에는 여러 개의 정규 표현식 디코더가 있을 수 있습니다. 디코더를 정의하는 순서는 중요합니다.로그 파일의 행과 일치하는 첫 번째 디코더는 해당 행을 디코딩하는 데 사용되는 디코더입니다.

이 예제에서는 일반 표현식 디코더를 사용하여 탭으로 구분된 텍스트 파일에서 데이터 필드를 추출하는 방법을 보여 줍니다. 탭 구분 기호로 구분된 디코더를 정의하여 동일한 결과를 얻을 수 있습니다.

![](assets/cfg_LogProcessingInclude_RegExpDecoder.png)

용어 및 구문을 포함한 일반 표현식 디코더에 대한 자세한 내용은 [정규 표현식](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c)을 참조하십시오.

## 구분된 디코더 {#section-7e0a23decdbc4c75ae750a42446997a6}

구분된 디코더는 필드가 단일 문자로 구분된 로그 파일을 디코딩합니다. 필드 수는 구분된 파일의 열 수와 일치해야 합니다.그러나 모든 필드에 이름을 지정할 필요는 없습니다. 필드를 비워 두면 로그 파일에 열이 여전히 필요하지만 디코더에서는 이를 무시합니다.

**텍스트 파일 디코더 그룹에 구분된 디코더를 추가하려면**

1. [기존 데이터 세트 포함 파일 편집](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077)에 설명된 대로 [!DNL Log Processing Dataset Include] 파일을 열고 텍스트 파일 디코더 그룹을 추가합니다. 테이블 항목 [디코더 그룹](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab)을 참조하십시오.

1. 새로 만든 디코더 그룹 아래의 **[!UICONTROL Decoders]**&#x200B;을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL Delimited]**&#x200B;를 클릭합니다.

1. 다음 정보를 지정합니다.

   * **필드:** 로그 파일의 필드 목록입니다. 여기에 정의된 필드를 데이터 세트 구성의 변형 단계로 전달하려면 해당 필드가 데이터 세트에 대한 [!DNL Log Processing Dataset Include] 파일 중 하나의 필드 매개 변수에 나열되어야 합니다. 사용자 정의 필드 이름은 &quot;x-&quot;로 시작해야 합니다.

   * **구분 기호:** 출력 파일의 필드를 구분하는 데 사용되는 문자입니다.

1. 그룹에 추가하려는 다른 디코더에 대해 4단계와 5단계를 반복합니다.
1. [!DNL Log Processing Dataset Include] 파일을 저장하려면 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;를 클릭합니다.

1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 [!DNL User] 열의 파일 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;를 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 데이터 세트 포함 파일이 속한 상속된 프로필입니다.

>[!NOTE]
>
>이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰여지기 때문에 수정된 구성 파일을 Adobe에서 제공하는 내부 프로파일에 저장하지 마십시오.

이 예에서는 동영상에 대한 데이터가 포함된 쉼표로 구분된 텍스트 파일에서 데이터 필드를 추출하기 위해 구분된 디코더를 사용하는 방법을 보여 줍니다.

![](assets/cfg_LogProcessingInclude_DelimitedDecoder.png)
