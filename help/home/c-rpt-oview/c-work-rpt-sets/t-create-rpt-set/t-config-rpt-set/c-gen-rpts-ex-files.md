---
description: 보고서를 Excel 파일로 생성하는 정보입니다.
title: 보고서를 Microsoft Excel 파일로 생성
uuid: 0717a916-93d6-4b8e-a2ff-e9179ba4a66e
exl-id: 4e644867-db5e-4ca9-a2bf-1193e031f2bf
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 4%

---

# 보고서를 Microsoft Excel 파일로 생성{#generating-reports-as-microsoft-excel-files}

보고서를 Excel 파일로 생성하는 정보입니다.

다음 요구 사항을 충족해야 합니다.

* Microsoft Excel은 [!DNL Report Server]과 동일한 컴퓨터에 설치해야 합니다.
* [!DNL Report Server] 프로세스가 실행 중인 사용자 계정에는 Microsoft Excel에 액세스할 수 있는 권한이 있어야 합니다.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * 보고서를 Excel 파일로 생성하면 새 Excel 인스턴스가 열립니다. 이 프로세스에 대한 자세한 내용은 [http://support.microsoft.com/kb/257757](http://support.microsoft.com/kb/257757)을 참조하십시오.
   >    * Data Workbench는 256개 이상의 열과 65,536개의 데이터 행을 지원하지만 Microsoft Excel은 지원하지 않습니다.


이러한 요구 사항이 충족되면 [!DNL Report Server]은(는) 자동으로 Microsoft Excel을 시작하고 특정 시각화, 차원 및 값 범례, 텍스트 주석에서 데이터를 워크시트당 하나의 시각화가 있는 새 Excel 통합 문서로 출력합니다.

>[!NOTE]
>
>데이터는 그래프, 경로 브라우저, 프로세스 맵, 산포도, 전구에서 내보내지지 않습니다.

시각화에 대해 [!DNL Custom Title]을 지정하지 않은 경우 창 유형(예: 동영상 테이블)이 워크시트 이름으로 사용됩니다.

시각화를 위해 [!DNL Custom Titles] 을 지정하는 방법에 대한 자세한 내용은 [Data Workbench 클라이언트 안내서](https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html?lang=ko-KR)를 참조하십시오.

## 템플릿 파일 사용 {#section-40ab11916f464b1a88214ab969da6751}

템플릿 Excel( [!DNL .xls] 또는 [!DNL .xlsx]) 파일을 사용하여 보고서를 Excel 파일로 생성할 수도 있습니다. 템플릿 파일을 사용하면 보고서가 생성될 때마다 데이터에 서식을 지정하는 데 걸리는 시간을 줄일 수 있습니다.

이 템플릿 파일은 [!DNL .xlt] 파일이 아닌 [!DNL .xls] 또는 [!DNL .xlsx] 파일이어야 합니다.

각 개별 보고서에 대한 템플릿, 모든 보고서에 대한 일반 템플릿 또는 두 보고서의 조합을 정의하도록 선택할 수 있습니다. 이 두 항목은 함께 사용할 수 없으므로 일반 템플릿을 정의한 다음 특정 템플릿도 정의할 수 있습니다.

모든 보고서에 사용하는 일반 템플릿을 사용하여 보고서를 생성하려면 해당 보고서 세트 파일의 [!DNL Report.cfg]에 있는 기본 Excel 템플릿 매개 변수에서 해당 Excel 파일의 이름을 지정한 다음 해당 보고서 세트의 [!DNL Report.cfg](*Data Workbench 설치 디렉토리*\*ProfileName*\Reports\*ReportSetName*)과 동일한 폴더에 템플릿 파일을 배치해야 합니다. 이 매개 변수에 대한 자세한 내용은 [Report.cfg 매개 변수](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff)를 참조하십시오.

보고서에 고유한 템플릿을 사용하여 보고서를 생성하려면 Excel 파일의 이름을 보고서 작업 공간( [!DNL .vw]) 파일과 동일하게 지정한 다음 보고서 작업 공간( [!DNL .vw]) 파일과 동일한 폴더에 템플릿 파일을 배치해야 합니다.

보고서가 생성되면 템플릿의 기존 탭 시트(각각 하나의 시각화를 나타내는)가 보고서의 가장 최근 데이터로 다시 채워지는 반면, 탭 시트로 템플릿에 존재하지 않는 새 창은 무시됩니다. 템플릿 파일의 다른 탭 시트는 변경되지 않은 상태로 유지됩니다.

또한 보고서 생성 시 자동으로 실행할 서식 파일 Excel 파일에 매크로가 정의되어 있으면 매크로 이름을 &quot;VSExport&quot;로 지정합니다.
