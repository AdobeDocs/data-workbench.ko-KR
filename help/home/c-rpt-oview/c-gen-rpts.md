---
description: 작업 공간을 처리하고 보고서로 지정하여 보고서를 생성합니다.
title: 보고서 생성
uuid: 90bc42b3-d7f2-46f2-8c68-5c682d163f3c
exl-id: 8e5765e8-71b6-4716-96fe-5c7f69407295
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 9%

---

# 보고서 생성{#generating-reports}

작업 공간을 처리하고 보고서로 지정하여 보고서를 생성합니다.

[!DNL Report] 에서는 파일 [!DNL Every] 의 매개 변수에 설정된 간격( [!DNL Report.cfg] 예: 매일 보고서를 처리하는  [!DNL "day])과 다른  [!DNL Report.cfg] 파일 설정을 기반으로 보고서를 생성합니다.

보고서를 생성하는 동안 특정 보고서의 축소판 아래에 있는 [!DNL Reports] 탭에 완료율이 표시됩니다. 보고서 생성 중에 [!DNL Report]에 문제가 발생하면 보고서 세트 폴더의 [!DNL Reports] 탭에 가장 최근 오류 메시지가 표시됩니다. [!DNL Report]에서 특정 보고서에 대한 오류가 발생하면 집합의 다른 보고서를 계속 처리합니다.

[!DNL Report.cfg] 파일의 [!DNL Report Types] 매개 변수를 사용하여 다음 형식 중 하나 또는 모두 형식의 보고서 세트에서 보고서를 생성할 수 있습니다.

* Microsoft Excel 파일( [!DNL .xls] 또는 [!DNL .xlsx])
* 휴대용 네트워크 그래픽 파일( [!DNL .png])
* 축소판( [!DNL .jpg])

지정된 출력 유형과 함께 [!DNL Report] 은 보고서와 동일한 이름의 [!DNL .xml] 파일을 만듭니다. 이 *`<report name>`*.xml 파일에는 보고서의 축소판 아래 [!DNL Reports] 탭에 Data Workbench에 표시되는 보고서에 대한 설명이 포함되어 있습니다. 이렇게 하면 설명을 보고 포털을 통해 보고서를 배포할 때 사용할 수 있습니다. [!DNL Report Portal]에 대한 자세한 내용은 [보고서 포털에서 작업](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35)을 참조하십시오.

>[!NOTE]
>
>내부 지표를 재정의하는 경우 시스템이 잘못된 값 때문에 예기치 않게 동작합니다. 지표를 100% 읽지 못하면 보고서가 생성되지 않습니다. 지표 정의를 변경하지 않는 것이 좋습니다.
