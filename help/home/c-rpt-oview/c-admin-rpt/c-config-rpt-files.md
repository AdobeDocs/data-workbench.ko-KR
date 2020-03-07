---
description: 보고서 포털에서는 보고서 서버에서 생성된 보고서를 Excel 파일(.xls 또는 .xlsx) 또는 .png 파일로 볼 수 있습니다.
solution: Analytics
title: Report.cfg 파일 구성
topic: Data workbench
uuid: b6ce1621-283f-458d-a88d-a062539d243b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Report.cfg 파일 구성{#configuring-report-cfg-files}

보고서 포털에서는 보고서 서버에서 생성된 보고서를 Excel 파일(.xls 또는 .xlsx) 또는 .png 파일로 볼 수 있습니다.

에 보고서 세트를 표시하려면 [!DNL Report Portal]해당 보고서 세트에 대한 [!DNL Report.cfg] 파일에서 다음 매개 변수를 설정해야 합니다.

* 매개 **[!UICONTROL Output Root]** 변수에서 포털에 사용되는 웹 서버의 문서 루트를 지정합니다.
* 매개 **[!UICONTROL Report Types]** 변수에서 Excel, png 및/또는 축소판을 생성할 보고서 유형으로 지정합니다.

지정한 형식으로 보고서를 [!DNL Report Server] 생성할 때 웹 서버의 문서 루트에 해당 파일을 배치합니다. 이 루트는 설치 중에 보고서에 액세스하도록 구성하는 [!DNL Report Portal] 곳입니다.

특정 매개 변수에 대한 자세한 내용은 Report.cfg 매개 [!DNL Report.cfg] 변수를 참조하십시오 [](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
