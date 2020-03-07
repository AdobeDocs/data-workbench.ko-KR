---
description: 작업 영역을 처리하고 보고서로 지정하여 보고서를 생성합니다.
solution: Analytics
title: 보고서 생성
topic: Data workbench
uuid: 90bc42b3-d7f2-46f2-8c68-5c682d163f3c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 생성{#generating-reports}

작업 영역을 처리하고 보고서로 지정하여 보고서를 생성합니다.

[!DNL Report] 에서는 [!DNL Every] 파일(예: 일별 보고서 처리 [!DNL Report.cfg] &quot;와 같이)의 매개 변수에 설정된 간격으로 보고서를 생성하고 다른 [!DNL "day][!DNL Report.cfg] 파일 설정에 따라 보고서를 생성합니다.

보고서를 생성하는 동안 특정 보고서의 축소판 아래 [!DNL Reports] 탭에 완료 비율이 표시됩니다. 보고서 생성 중 문제가 [!DNL Report] 발생하면 보고서 세트 폴더의 [!DNL Reports] 탭에 최신 오류 메시지가 표시됩니다. 특정 보고서에 대한 오류가 [!DNL Report] 발생하면 세트의 다른 보고서를 계속 처리합니다.

파일의 매개 변수를 사용하여 다음 형식 중 하나 또는 모든 형식으로 보고서 세트에서 보고서를 생성할 수 [!DNL Report Types] 있습니다 [!DNL Report.cfg] .

* Microsoft Excel 파일( [!DNL .xls] 또는 [!DNL .xlsx])
* 휴대용 네트워크 그래픽 파일( [!DNL .png])
* 축소판 ( [!DNL .jpg])

지정된 출력 유형과 함께 [!DNL Report] 보고서와 같은 [!DNL .xml] 파일을 만듭니다. 이 *`<report name>`*.xml 파일에는 보고서의 축소판 아래 [!DNL Reports] 탭의 데이터 워크벤치에 표시되는 보고서에 대한 설명이 들어 있습니다. 이렇게 하면 보고 포털을 통해 보고서를 배포할 때 설명을 사용할 수 있습니다. 자세한 내용은 [!DNL Report Portal]보고서 포털 [작업을 참조하십시오](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35).

>[!NOTE]
>
>내부 지표를 재정의하는 경우 잘못된 값으로 인해 시스템이 예기치 않게 동작합니다. 지표가 100%를 읽지 않으면 보고서가 생성되지 않습니다. 지표 정의를 변경하지 않는 것이 좋습니다.
