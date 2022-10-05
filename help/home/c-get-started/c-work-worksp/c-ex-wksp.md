---
description: 작업 공간을 .png 이미지 파일로 내보내거나 특정 창에서 Excel(.xls 또는 .xlsx) 파일로 데이터를 내보낼 수 있습니다.
title: 작업 영역 내보내기
uuid: 59ea6e46-d2e9-41f9-9c8f-e3071eb65424
exl-id: 87416ddf-2ac0-4f95-ae8e-71051061c757
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 1%

---

# 작업 영역 내보내기{#export-a-workspace}

{{eol}}

작업 공간을 .png 이미지 파일로 내보내거나 특정 창에서 Excel(.xls 또는 .xlsx) 파일로 데이터를 내보낼 수 있습니다.

## 작업 공간을 PNG 파일로 내보내기 {#section-f9fbe0f0a1c341e2b063cce106cac35e}

작업 공간의 스냅샷을 휴대용 네트워크 그래픽 형식(`.png` 파일 참조). 다음 색상 옵션은 작업 공간을 `.png` 파일:

* **검은색 배경** 표시된 대로 작업 공간을 복사합니다.
* **흰색 배경** 작업 영역의 요소를 색상으로 복사하고 흰색 배경에 표시합니다.
* **흰색 배경(B&amp;W)** 작업 영역의 요소를 회색 음영으로 복사하고 흰색 배경에 표시합니다.

**작업 영역을 .png 파일로 내보내려면**

작업 공간의 제목 표시줄 메뉴에서 **[!UICONTROL Export]** > **[!UICONTROL Export PNG]** > *&lt;**[!UICONTROL color option]**>*.

[!UICONTROL Save Image As] 대화 상자가 표시됩니다.

파일을 저장할 디렉토리로 이동하여 필요한 경우 파일 이름을 변경한 다음 **[!UICONTROL Save]**.

## 작업 공간 데이터를 Microsoft Excel로 내보내기 {#section-fe214e3dbc364d2eba3834d62d295acb}

작업 공간을 Excel로 내보낼 때 Data Workbench은 특정 시각화, 차원 및 값 범례, 텍스트 주석에서 워크시트당 하나의 시각화가 있는 새 Excel 통합 문서로 데이터를 내보냅니다.

작업 공간 및 개별 창을 Microsoft Excel로 내보내려면 다음 요구 사항을 충족해야 합니다.

* Microsoft Excel은 Data Workbench과 동일한 컴퓨터에 설치해야 합니다.
* Data Workbench 프로세스가 실행 중인 사용자 계정에는 Microsoft Excel에 액세스할 수 있는 권한이 있어야 합니다.

>[!NOTE]
>
>* 데이터를 Excel 파일로 내보낼 때 새 Excel 인스턴스가 열립니다. 이 프로세스에 대한 자세한 내용은 [https://support.microsoft.com/kb/257757](https://support.microsoft.com/kb/257757).
>* Data Workbench은 256개 이상의 열과 65,536개의 데이터 행을 지원하지만 8.0 이전 버전의 Microsoft Excel은 지원하지 않습니다.
>


이러한 요구 사항이 충족되면 Data Workbench은 자동으로 Microsoft Excel을 시작하고 데이터를 새 Excel 통합 문서로 내보냅니다. 데이터는 다음 시각화에서 내보내지지 않습니다. 그래프, 경로 브라우저, 프로세스 맵, 산포도, 전구.

## 사용자 지정 제목 적용 {#section-a332e157554546cb8e88922a8d7a4fa2}

창의 사용자 지정 제목을 지정하지 않은 경우 [!UICONTROL Export] 메뉴, [!UICONTROL Export title] 나열된 워크시트 이름(예: 도시 테이블)으로 사용됩니다.

1. 창의 위쪽 테두리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Custom title]** 필드.
1. 창에 적용할 제목을 입력합니다.

   ![](assets/mnu_window_TitleBar_Export.png)

>[!NOTE]
>
>에 하이픈(-)을 입력하는 경우 [!UICONTROL Custom title] 필드에서 이 시각화는 작업 공간으로 내보내지지 않습니다.

작업 영역을 Excel로 내보내면 이 창의 데이터가 포함된 워크시트의 이름은 의 제목 대신 지정한 제목을 사용하여 지정됩니다 [!UICONTROL Export title] 필드.

## 작업 공간이나 사이드바를 Excel로 내보내기 {#section-360438b66d5f4734826ab463b4a01a75}

**작업 공간 데이터를 새 페이지로 내보내려면 [!DNL .xls] 또는 [!DNL .xlsx] 파일**

1. 작업 공간의 제목 표시줄에서 **[!UICONTROL Export]** > **[!UICONTROL Export]**.
1. 작업 공간, 사이드바 또는 둘 다 내보내지 여부를 지정합니다.

## 템플릿 Excel 파일로 내보내기 {#section-814772929ca64cf6b92b89d3fdd02302}

작업 공간의 데이터를 템플릿 Excel 파일(`.xls` 또는 `.xlsx`). 템플릿 파일을 사용하면 작업 공간을 내보낼 때마다 데이터에 서식을 지정하는 데 걸리는 시간을 줄일 수 있습니다.

>[!NOTE]
>
>이 템플릿 파일은 `.xls` 또는 `.xlsx` 파일, 아님 `.xlt` 파일.

데이터를 내보내면 템플릿의 기존 탭 시트(각각 하나의 시각화를 나타내는)가 작업 공간의 최신 데이터로 다시 채워지는 반면, 탭 시트로 템플릿에 없는 새 창은 무시됩니다. 템플릿 파일의 다른 탭 시트는 변경되지 않은 상태로 유지됩니다.

또한 보고서 생성 시 자동으로 실행할 서식 파일 Excel 파일에 매크로가 정의되어 있으면 매크로 이름을 &quot;VSExport&quot;로 지정합니다.

내보낸 캠페인 데이터를 Excel 파일의 다른 탭 시트에 있는 파이 차트의 테이블 시각화에 사용하고 이 정보를 매주 업데이트하려고 한다고 가정합니다. 데이터를 업데이트할 때마다 테이블의 탭 시트에서 원형 차트의 탭 시트로 참조를 다시 작성하지 않아도 되도록 템플릿을 사용할 수 있습니다. 테이블 데이터는 내보낼 때 업데이트되므로 원형 차트를 자동으로 업데이트합니다.

**작업 공간 데이터를 템플릿으로 내보내려면 [!DNL .xls] 또는 [!DNL .xlsx] 파일**

1. 작업 공간의 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Export]** > **[!UICONTROL Export to Excel from Template]**.
1. 작업 공간, 사이드바 또는 둘 다를 내보내지 여부를 지정합니다.

   다음 [!UICONTROL Select a template worksheet] 대화 상자가 열립니다.

1. 다음 단계 중 하나를 적절히 완료합니다.

   * 를 사용 중인 경우 `.xls` 템플릿 파일:

      1. 서식 파일로 이동하여 선택합니다 `.xls` 파일.
      1. 클릭 **[!UICONTROL Open]**.
   * 를 사용 중인 경우 `.xlsx` 템플릿 파일:

      1. 템플릿 파일의 위치를 찾습니다. 다음 `.xlsx` 파일 이름이 표시되지 않습니다.
      1. 에서 [!UICONTROL File name] 필드, 유형 `.xlsx` 을(를) 클릭합니다. **[!UICONTROL Open]**. 모두 `.xlsx` 파일 이름은 파일 목록에 표시됩니다.

      1. 템플릿을 선택합니다 `.xlsx` 파일.
      1. 클릭 **[!UICONTROL Open]**.
