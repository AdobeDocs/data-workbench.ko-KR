---
description: 작업 영역을 .png 이미지 파일로 내보내거나 특정 창에서 Excel(.xls 또는 .xlsx) 파일로 데이터를 내보낼 수 있습니다.
title: 작업 영역 내보내기
uuid: 59ea6e46-d2e9-41f9-9c8f-e3071eb65424
exl-id: 87416ddf-2ac0-4f95-ae8e-71051061c757
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 1%

---

# 작업 영역 내보내기{#export-a-workspace}

작업 영역을 .png 이미지 파일로 내보내거나 특정 창에서 Excel(.xls 또는 .xlsx) 파일로 데이터를 내보낼 수 있습니다.

## 작업 영역을 PNG 파일 {#section-f9fbe0f0a1c341e2b063cce106cac35e}로 내보내기

작업 영역의 스냅숏을 이동식 네트워크 그래픽 형식(`.png` 파일)으로 저장할 수 있습니다. 작업 영역을 `.png` 파일로 저장할 때 다음 색상 옵션을 사용할 수 있습니다.

* **검정** 배경이 표시된 대로 작업 영역을 복사합니다.
* **흰색** 배경색 작업 영역의 요소를 복사하여 흰색 배경에 표시합니다.
* **흰색 배경(흑백)** 은 작업 영역의 요소를 회색 음영으로 복사하고 흰색 배경에 표시합니다.

**작업 영역을 .png 파일로 내보내려면**

작업 영역의 제목 표시줄 메뉴에서 **[!UICONTROL Export]** > **[!UICONTROL Export PNG]** > *&lt;**[!UICONTROL color option]***&#x200B;를 클릭합니다.

[!UICONTROL Save Image As] 대화 상자가 나타납니다.

파일을 저장할 디렉토리로 이동하여 필요한 경우 파일 이름을 변경하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

## 작업 영역 데이터를 Microsoft Excel {#section-fe214e3dbc364d2eba3834d62d295acb}로 내보내기

작업 영역을 Excel로 내보낼 때 Data Workbench은 특정 시각화, 차원 및 값 범례, 텍스트 주석의 데이터를 워크시트당 하나의 시각화가 있는 새 Excel 통합 문서로 내보냅니다.

작업 영역 및 개별 창을 Microsoft Excel로 내보내려면 다음 요구 사항을 충족해야 합니다.

* Microsoft Excel을 Data Workbench과 동일한 컴퓨터에 설치해야 합니다.
* Data Workbench 프로세스가 실행 중인 사용자 계정에는 Microsoft Excel에 액세스할 수 있는 권한이 있어야 합니다.

>[!NOTE]
>
>* 데이터를 Excel 파일로 내보내면 새로운 Excel 인스턴스가 열립니다. 이 프로세스에 대한 자세한 내용은 [http://support.microsoft.com/kb/257757](http://support.microsoft.com/kb/257757)을 참조하십시오.
>* Data Workbench은 256개 이상의 열과 65,536개의 데이터 행을 지원하지만 8.0 이전의 Microsoft Excel 버전은 지원하지 않습니다.
>



이러한 요구 사항이 충족되면 Data Workbench은 자동으로 Microsoft Excel을 시작하고 데이터를 새 Excel 통합 문서로 내보냅니다. 데이터는 다음 시각화에서 내보내지지 않습니다.그래프, 경로 브라우저, 프로세스 맵, 분산형 플롯 및 글로브.

## 사용자 정의 제목 {#section-a332e157554546cb8e88922a8d7a4fa2} 적용

[!UICONTROL Export] 메뉴에서 윈도우에 대한 사용자 정의 제목을 지정하지 않은 경우, 나열된 [!UICONTROL Export title](예: 도시 테이블)이 워크시트 이름으로 사용됩니다.

1. 창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Custom title]** 필드를 클릭합니다.
1. 창에 적용할 제목을 입력합니다.

   ![](assets/mnu_window_TitleBar_Export.png)

>[!NOTE]
>
>[!UICONTROL Custom title] 필드에 하이픈(-)을 입력하면 이 시각화는 작업 영역으로 내보내지지 않습니다.

작업 영역을 Excel로 내보내면 이 창에 대한 데이터가 포함된 워크시트의 이름은 [!UICONTROL Export title] 필드의 제목 대신 지정한 제목을 사용하여 지정됩니다.

## 작업 공간 또는 사이드바를 Excel {#section-360438b66d5f4734826ab463b4a01a75}로 내보내기

**작업 영역 데이터를 새  [!DNL .xls] 또는  [!DNL .xlsx] 파일로 내보내려면**

1. 작업 영역의 제목 표시줄에서 **[!UICONTROL Export]** > **[!UICONTROL Export]**&#x200B;을 클릭합니다.
1. 작업 공간, 사이드바 또는 둘 다를 내보낼지 지정합니다.

## 템플릿 Excel 파일 {#section-814772929ca64cf6b92b89d3fdd02302}(으)로 내보내기

작업 영역의 데이터를 템플릿 Excel 파일(`.xls` 또는 `.xlsx`)로 내보낼 수 있습니다. 템플릿 파일을 사용하면 작업 영역을 내보낼 때마다 데이터의 서식을 지정하는 데 걸리는 시간을 줄일 수 있습니다.

>[!NOTE]
>
>이 템플릿 파일은 `.xlt` 파일이 아닌 `.xls` 또는 `.xlsx` 파일이어야 합니다.

데이터를 내보낼 때 템플릿에 있는 기존 탭 시트(각 시각화 표시)는 작업 공간에서 최근 데이터로 채워지고, 템플릿에 탭 시트로 표시되지 않는 새 창은 무시됩니다. 템플릿 파일의 다른 탭 시트는 변경되지 않습니다.

또한 보고서가 생성되면 자동으로 실행할 매크로를 템플릿 Excel 파일에 정의한 경우 매크로 이름을 &quot;VSExport&quot;로 지정합니다.

Excel 파일의 다른 탭 시트에서 파이 차트에 있는 표 시각화에서 내보낸 캠페인 데이터를 사용하고 매주 이 정보를 업데이트하려고 한다고 가정해 봅시다. 데이터를 업데이트할 때마다 테이블의 탭 시트에서 파이 차트의 탭 시트에 대한 참조를 다시 만들지 않아도 되도록 템플릿을 사용할 수 있습니다. 테이블 데이터는 내보낼 때 업데이트되므로 원형 차트가 자동으로 업데이트됩니다.

**작업 공간 데이터를 템플릿 또는  [!DNL .xls] 파일로  [!DNL .xlsx] 내보내려면**

1. 작업 영역의 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Export]** > **[!UICONTROL Export to Excel from Template]**&#x200B;을 클릭합니다.
1. 작업 공간, 사이드바 또는 둘 다를 내보낼지 지정합니다.

   [!UICONTROL Select a template worksheet] 대화 상자가 열립니다.

1. 다음 단계 중 하나를 적절히 완료하십시오.

   * `.xls` 템플릿 파일을 사용하는 경우:

      1. 템플릿 `.xls` 파일을 찾아 선택합니다.
      1. 클릭 **[!UICONTROL Open]**.
   * `.xlsx` 템플릿 파일을 사용하는 경우:

      1. 템플릿 파일의 위치를 찾습니다. `.xlsx` 파일 이름이 표시되지 않습니다.
      1. [!UICONTROL File name] 필드에 `.xlsx`을 입력하고 **[!UICONTROL Open]**&#x200B;를 클릭합니다. 모든 `.xlsx` 파일 이름이 파일 목록에 표시됩니다.

      1. 템플릿 `.xlsx` 파일을 선택합니다.
      1. 클릭 **[!UICONTROL Open]**.
