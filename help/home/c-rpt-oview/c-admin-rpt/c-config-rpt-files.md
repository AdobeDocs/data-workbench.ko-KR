---
description: 보고서 포털에서 보고서 서버에서 생성된 보고서를 Excel 파일(.xls 또는 .xlsx) 또는 .png 파일로 볼 수 있습니다.
title: Report.cfg 파일 구성
uuid: b6ce1621-283f-458d-a88d-a062539d243b
exl-id: 5af5abaa-77bf-447b-b341-8f44e228f37a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---

# Report.cfg 파일 구성{#configuring-report-cfg-files}

보고서 포털에서 보고서 서버에서 생성된 보고서를 Excel 파일(.xls 또는 .xlsx) 또는 .png 파일로 볼 수 있습니다.

[!DNL Report Portal]에 보고서 세트를 표시하려면 해당 보고서 세트에 대한 [!DNL Report.cfg] 파일에서 다음 매개 변수를 설정해야 합니다.

* **[!UICONTROL Output Root]** 매개 변수에서 포털에 사용되는 웹 서버의 문서 루트를 지정합니다.
* **[!UICONTROL Report Types]** 매개 변수에서 생성할 보고서 유형으로 Excel, png 및/또는 축소판을 지정합니다.

[!DNL Report Server]이 지정한 형식의 보고서를 생성할 때 웹 서버의 문서 루트에 해당 파일을 배치합니다. 이 루트는 설치 중에 보고서에 액세스하기 위해 [!DNL Report Portal]을 구성하는 곳입니다.

특정 [!DNL Report.cfg] 매개 변수에 대한 자세한 내용은 [Report.cfg 매개 변수](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff)를 참조하십시오.
