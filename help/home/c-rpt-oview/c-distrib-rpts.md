---
description: 보고서가 생성되면 Report는 해당 Report.cfg 파일의 설정을 기반으로 세트에 보고서를 배포합니다.
title: 보고서 배포
uuid: 0e993635-1aa8-4314-91aa-b4f8f002fa09
exl-id: ead1d8ef-7319-4307-9155-0101a9c1959d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# 보고서 배포{#distributing-reports}

보고서가 생성되면 Report는 해당 Report.cfg 파일의 설정을 기반으로 세트에 보고서를 배포합니다.

[!DNL Report] 에서는 다음 방법을 사용하여 보고서를 세트로 배포할 수 있습니다.

* **이메일:** 보고서를 이메일(인라인 또는 첨부 파일)을 통해 Excel 파일,  [!DNL .png] 파일 또는 미리 보기로 배포하려면 보고서 세트의 파일에 메일 보고서 매개 변수를  [!DNL Report.cfg] 지정합니다. 이 세트의 모든 보고서는 지정된 수신자에게 하나의 메시지로 발송됩니다.

* **공유 디렉토리:** 보고서를 Excel 파일,  [!DNL .png] 파일 또는 공유 디렉토리에 축소판으로 배포하려면 보고서 세트의 파일에 있는 출력 루트 매개 변수에 디렉토리를  [!DNL Report.cfg] 지정합니다.

* **보고 포털:** 보고 포털을 사용하면 웹 브라우저를 통해 보고서를 볼 수 있습니다. Adobe의 [!DNL Report Portal]은 Excel 또는 [!DNL .png] 파일로 생성된 보고서를 표시하지만 축소판으로 생성된 보고서는 표시하지 않습니다( [!DNL .jpg]). 포털에 보고서를 배포하려면 보고서 세트의 [!DNL Report.cfg] 파일의 출력 루트 매개 변수에서 포털에 사용되는 웹 서버의 문서 루트를 지정하십시오. [!DNL Report Portal] 설치 및 사용에 대한 자세한 내용은 [보고서 포털에서 작업](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35)을 참조하십시오.

>[!NOTE]
>
>현재 [!DNL Report]에서 지원하는 출력을 읽으려면 원하는 형식으로 보고서를 표시할 수 있는 응용 프로그램이 있어야 합니다. 예를 들어 [!DNL .xlsx] 파일을 보려면 Microsoft Excel 2007 이상이 있어야 합니다.

이러한 생성 및 배포 옵션의 조합을 사용할 수도 있습니다. 예를 들어 [!DNL Report Types] 매개 변수를 설정하여 Excel 및 [!DNL .png] 파일로 보고서 세트를 생성한 다음 [!DNL Mail Report] 및 [!DNL Output Root] 매개 변수를 설정하면 해당 세트의 모든 보고서가 지정된 출력 디렉토리(포털에서 볼 수 있음)에 배포되어 수신자에게 전자 메일로 전송됩니다.

보고서 세트를 구성하는 단계는 [보고서 집합 작업](../../home/c-rpt-oview/c-work-rpt-sets/c-work-rpt-sets.md#concept-a5f078668e1245e684cb2a778c8803d5)을 참조하십시오. 특정 [!DNL Report.cfg] 매개 변수에 대한 자세한 내용은 [Report.cfg 매개 변수](../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff)를 참조하십시오.
