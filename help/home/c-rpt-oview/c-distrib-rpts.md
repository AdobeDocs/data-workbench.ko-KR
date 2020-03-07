---
description: 보고서가 생성되면 보고서는 Report.cfg 파일의 설정을 기반으로 세트에 보고서를 배포합니다.
solution: Analytics
title: 보고서 배포
topic: Data workbench
uuid: 0e993635-1aa8-4314-91aa-b4f8f002fa09
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 배포{#distributing-reports}

보고서가 생성되면 보고서는 Report.cfg 파일의 설정을 기반으로 세트에 보고서를 배포합니다.

[!DNL Report] 에서는 다음 방법을 사용하여 세트에 보고서를 배포할 수 있습니다.

* **이메일:** 보고서를 이메일(인라인 또는 첨부 파일)을 통해 Excel 파일 [!DNL .png] , 파일 또는 축소판으로 배포하려면 보고서 세트의 [!DNL Report.cfg] 파일에 메일 보고서 매개 변수를 지정합니다. 해당 세트의 모든 보고서는 지정된 수신자에게 하나의 메시지로 이메일로 전송됩니다.

* **공유 디렉토리:** 보고서를 Excel 파일, [!DNL .png] 파일 또는 축소판으로 공유 디렉토리에 배포하려면 보고서 세트의 [!DNL Report.cfg] 파일에서 출력 루트 매개 변수에 디렉토리를 지정합니다.

* **보고 포털:** 보고 포털을 통해 웹 브라우저를 통해 보고서를 볼 수 있습니다. Adobe [!DNL Report Portal] 는 Excel 또는 [!DNL .png] 파일로 생성된 보고서를 표시하지만 축소판으로 생성된 보고서는 표시하지 않습니다( [!DNL .jpg]). 포털에 보고서를 배포하려면 보고서 세트 [!DNL Report.cfg] 파일의 출력 루트 매개 변수에서 포털에 사용되는 웹 서버의 문서 루트를 지정합니다. 설치 및 사용에 대한 자세한 내용은 [!DNL Report Portal]보고서 포털 [작업을 참조하십시오](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35).

>[!NOTE]
>
>현재 에서 지원되는 출력을 읽으려면 [!DNL Report]원하는 형식으로 보고서를 표시할 수 있는 응용 프로그램이 있어야 합니다. 예를 들어 [!DNL .xlsx] 파일을 보려면 Microsoft Excel 2007 이상이 있어야 합니다.

이러한 생성 및 배포 옵션을 조합하여 사용할 수도 있습니다. 예를 들어, 보고서 세트를 Excel 및 [!DNL Report Types] 파일로 생성하도록 [!DNL .png] 매개 변수를 설정한 다음 [!DNL Mail Report]및 [!DNL Output Root] 매개 변수를 설정하면 해당 세트의 모든 보고서가 지정된 출력 디렉토리(포털에서 볼 수 있음)에 배포되고 한 개의 이메일로 수신자에게 전송됩니다.

보고서 세트를 구성하는 단계는 보고서 세트 [작업을 참조하십시오](../../home/c-rpt-oview/c-work-rpt-sets/c-work-rpt-sets.md#concept-a5f078668e1245e684cb2a778c8803d5). 특정 매개 변수에 대한 자세한 내용은 Report.cfg 매개 [!DNL Report.cfg] 변수를 참조하십시오 [](../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
