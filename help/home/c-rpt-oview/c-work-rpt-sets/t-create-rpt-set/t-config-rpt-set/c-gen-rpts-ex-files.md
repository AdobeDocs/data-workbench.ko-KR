---
description: 보고서를 Excel 파일로 생성하는 정보입니다.
solution: Analytics
title: 보고서를 Microsoft Excel 파일로 생성
topic: Data workbench
uuid: 0717a916-93d6-4b8e-a2ff-e9179ba4a66e
translation-type: tm+mt
source-git-commit: 2cba66a160fec9154796f093d04a422a5b0da265

---


# 보고서를 Microsoft Excel 파일로 생성{#generating-reports-as-microsoft-excel-files}

보고서를 Excel 파일로 생성하는 정보입니다.

다음 요구 사항을 충족해야 합니다.

* Microsoft Excel은 동일한 컴퓨터에 설치해야 합니다 [!DNL Report Server].
* 프로세스가 실행 중인 사용자 계정에는 Microsoft Excel에 액세스할 수 있는 권한이 있어야 합니다. [!DNL Report Server]

   >[!NOTE]
   >
   >
   >    
   >    
   >    * 보고서를 Excel 파일로 생성할 때 새 Excel 인스턴스를 엽니다. 이 프로세스에 대한 자세한 내용은 http://support.microsoft.com/kb/257757을 [참조하십시오](http://support.microsoft.com/kb/257757).
   >    * 데이터 워크벤치에서는 256개 이상의 열과 65,536개의 데이터 행을 지원하지만 Microsoft Excel에서는 지원하지 않습니다.


이러한 요구 사항이 충족되면 Microsoft Excel을 [!DNL Report Server] 자동으로 시작하고 특정 시각화, 차원 및 값 범례, 텍스트 주석의 데이터를 워크시트당 하나의 시각화로 새로운 Excel 통합 문서로 출력합니다.

>[!NOTE]
>
>데이터는 그래프, 경로 브라우저, 프로세스 맵, 산포도 및 글로브에서 내보내지지 않습니다.

시각화에 [!DNL Custom Title] 대해 지정하지 않은 경우 창 유형(예: 동영상 테이블)이 워크시트 이름으로 사용됩니다.

시각화에 [!DNL Custom Titles] 대한 지정에 대한 자세한 내용은 데이터 워크벤치 [클라이언트 안내서를 참조하십시오](https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html).

## 템플릿 파일 사용 {#section-40ab11916f464b1a88214ab969da6751}

템플릿 Excel( [!DNL .xls] 또는 [!DNL .xlsx]) 파일을 사용하여 보고서를 Excel 파일로 생성할 수도 있습니다. 템플릿 파일을 사용하면 보고서가 생성될 때마다 데이터의 서식을 지정하는 데 걸리는 시간을 줄일 수 있습니다.

이 템플릿 파일은 [!DNL .xls] 파일이 아닌 [!DNL .xlsx] 또는 [!DNL .xlt] 파일이어야 합니다.

각 개별 보고서에 대한 템플릿, 모든 보고서에 대한 일반 템플릿 또는 두 보고서의 조합을 정의하도록 선택할 수 있습니다. 이러한 두 항목은 함께 사용할 수 없으므로 일반 템플릿을 정의한 다음 특정 템플릿을 정의할 수도 있습니다.

모든 보고서에 사용하는 일반 템플릿을 사용하여 보고서를 생성하려면 해당 보고서 세트 파일의 기본 Excel 템플릿 매개 변수에 해당 Excel 파일의 이름을 [!DNL Report.cfg] 지정한 다음 해당 보고서 세트에 [!DNL Report.cfg] 대한 폴더(*데이터 워크벤치 설치 디렉토리*\*\Reports\*ReportSetName*)와 동일한 폴더에 템플릿 파일을 배치해야 합니다. 이 매개 변수에 대한 자세한 내용은 Report.cfg [매개 변수를 참조하십시오](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

보고서별 템플릿을 사용하여 보고서를 생성하려면 보고서 작업 영역( [!DNL .vw]) 파일과 동일한 이름을 Excel 파일로 지정한 다음 보고서 작업 영역( [!DNL .vw]) 파일과 같은 폴더에 템플릿 파일을 배치해야 합니다.

보고서가 생성되면 템플릿의 기존 탭 시트(각 시각화 표시)가 보고서의 최신 데이터로 다시 채워지지만 탭 시트로 템플릿에 없는 새 창은 무시됩니다. 템플릿 파일의 다른 탭 시트는 변경되지 않습니다.

또한 템플릿 Excel 파일에 보고서를 생성할 때 자동으로 실행하려는 매크로가 정의된 경우 매크로 이름을 &quot;VSExport&quot;로 지정합니다.
