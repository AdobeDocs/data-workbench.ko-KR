---
description: 필드 뷰어를 종속성 맵에서 콜아웃으로 열거나 관리 메뉴에서 독립형 시각화로 열 수 있습니다.
title: 필드 뷰어 만들기
uuid: df48e728-96f9-4432-82c8-f8047840ffb9
exl-id: a2563dbb-1d1f-4ed8-b73b-6ac7a2687405
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 2%

---

# 필드 뷰어 만들기{#create-a-field-viewer}

필드 뷰어를 종속성 맵에서 콜아웃으로 열거나 관리 메뉴에서 독립형 시각화로 열 수 있습니다.

## 종속성 맵 {#section-040cb83c902b49c48b841d35abc127e5}에서 필드 뷰어 만들기

종속성 맵에서 필드 뷰어를 열면([필드 뷰어 열기](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-opn-field-vwrs.md#concept-0f0738ac50804a33818487222c337c27)에 표시) 마우스 오른쪽 단추를 클릭한 로그 소스, 변형 또는 차원을 기반으로 뷰어가 자동으로 채워집니다. 로그 소스 또는 변환의 경우 뷰어의 필드는 로그 소스 또는 변환의 입력 또는 출력입니다. 차원의 경우 필드는 차원의 입력입니다. 원하는 대로 필드를 추가하고 제거할 수 있습니다.

## 필드 뷰어를 독립형 시각화 {#section-11d10e46631d4fdca45d7534336e1e80}(으)로 만듭니다.

필드 뷰어를 독립형 시각화로 열면 [!DNL Log Processing Field Viewer] 또는 [!DNL Transformation Field Viewer]을 만들 수 있습니다. 뷰어가 비어 있으므로 뷰어에 원하는 필드를 추가해야 합니다. [!DNL Log Processing Field Viewer]의 경우 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing dataset include] 파일의 필드를 추가할 수 있습니다. [!DNL Transformation Field Viewer]의 경우 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation dataset include] 파일의 필드를 추가할 수 있습니다.

구성 및 포함 파일에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

## 필드 {#section-9c0d4f5735a044a8b21dc7a99c63a59a} 추가 및 제거

**필드 뷰어에 필드를 추가하려면**

* 필드 뷰어 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Fields]** > *&lt;**[!UICONTROL field name]*** > *&lt;**[!UICONTROL instance]***&#x200B;를 클릭합니다.

   -또는-

* 필드 뷰어의 기존 열 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Fields]** > *&lt;**[!UICONTROL field name]**>* > *&lt;**[!UICONTROL instance]***&#x200B;를 클릭합니다.

필드 이름은 필드의 이름을 참조하고, 인스턴스는 데이터 집합 구성에서 데이터 집합 처리 단계 또는 변환과 같이 필드가 사용되는 위치를 나타냅니다. 일부 필드는 데이터 집합 구성 내의 여러 위치에서 사용되므로(예: 필드를 여러 변형으로 수정할 수 있음) 필드 뷰어에 추가할 필드 인스턴스를 선택해야 합니다.

사용 가능한 필드 목록에서 뷰어에 이미 표시된 필드의 왼쪽에 X가 나타납니다.

**필드 뷰어에서 필드를 제거하려면**

* 제거할 필드의 열 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Remove Field]** 을 클릭합니다.
