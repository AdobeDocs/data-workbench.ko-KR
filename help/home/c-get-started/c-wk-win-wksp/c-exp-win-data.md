---
description: 특정 창의 데이터를 Excel 파일(.xls 또는 .xlsx)이나 탭으로 구분된 값 파일(.tsv)로 내보낼 수 있습니다.
title: 창 데이터 내보내기
uuid: 71a93f35-1096-41ae-8808-e5b94813a52c
exl-id: ab931453-d366-4d3a-990e-7a368328da2d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 1%

---

# 창 데이터 내보내기{#export-window-data}

특정 창의 데이터를 Excel 파일(.xls 또는 .xlsx)이나 탭으로 구분된 값 파일(.tsv)로 내보낼 수 있습니다.

데이터는 그래프, 경로 브라우저, 프로세스 맵, 산포도, 전구에서 내보내지지 않습니다.

## 창 데이터를 Microsoft Excel {#section-b660adf7f4f64a2b9be7287c591b67b0}로 내보내기

개별 창 데이터를 Microsoft Excel로 내보내려면 다음 요구 사항을 충족해야 합니다.

* Microsoft Excel은 Data Workbench과 동일한 컴퓨터에 설치해야 합니다.
* Data Workbench 프로세스가 실행 중인 사용자 계정에는 Microsoft Excel에 액세스할 수 있는 권한이 있어야 합니다.
* 데이터를 Excel 파일로 내보낼 때 새 Excel 인스턴스가 열립니다.
* Data Workbench은 256개 이상의 열과 65,536개의 데이터 행을 지원하지만 8.0 이전 버전의 Microsoft Excel은 지원하지 않습니다.

이러한 요구 사항이 충족되면 Data Workbench은 Microsoft Excel을 자동으로 시작하고 **[!UICONTROL Export To Excel]** 메뉴 옵션을 선택하면 데이터를 새 Excel 통합 문서로 내보냅니다.

**창 데이터를 .xls 또는 .xlsx 파일로 내보내려면**

창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Export]** > **[!UICONTROL Export to Excel]** 를 클릭합니다.

![](assets/mnu_window_TitleBar_Export.png)

내보낸 데이터가 포함된 새 통합 문서가 열립니다. 다음 섹션에 설명된 대로 사용자 지정 제목을 제공하지 않은 한, 이 통합 문서는 [!DNL Export title] (위의 예에서 일 테이블)을 사용하여 이름이 지정됩니다.

## 사용자 지정 제목 {#section-2a6559df812a470685e43923b7b9024e} 적용

[!DNL Export] 메뉴에서 [!DNL Custom title] 필드를 사용하여 창의 사용자 지정 제목을 제공하는 경우 Data Workbench이 데이터를 내보내는 워크시트의 이름은 [!DNL Export title] 필드(위의 예에서 일 테이블)의 제목 대신 이 사용자 지정 제목을 사용하여 지정됩니다.

**시각화에 사용자 지정 제목을 적용하려면**

1. 창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Custom title]** 필드를 클릭합니다.
1. you

![](assets/mnu_window_TitleBar_Export.png)

시각화를 Excel로 내보내면 이 창의 데이터가 포함된 워크시트의 이름은 [!DNL Export title] 필드에서 제목 대신 지정한 제목을 사용하여 지정됩니다.

## 창 데이터를 TSV 파일 {#section-93c6b24f7338430aaf5a63b99b9489e8}로 내보내기

**창을 .tsv 파일로 내보내려면**

창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Export]** > **[!UICONTROL Export TSV]** 를 클릭합니다.

1. [!DNL Save Window] 대화 상자가 나타납니다.
1. 파일을 저장할 디렉토리로 이동합니다. 필요한 경우 파일 이름을 변경하고 **[!UICONTROL Save]** 을 클릭합니다.
