---
description: 작업 공간을 처리하고 보고서로 지정하여 보고서를 생성합니다.
title: 보고서 생성
uuid: 90bc42b3-d7f2-46f2-8c68-5c682d163f3c
exl-id: 8e5765e8-71b6-4716-96fe-5c7f69407295
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 9%

---

# 보고서 생성{#generating-reports}

{{eol}}

작업 공간을 처리하고 보고서로 지정하여 보고서를 생성합니다.

[!DNL Report] 는 [!DNL Every] 의 매개 변수 [!DNL Report.cfg] 파일(예: [!DNL "day],&quot;는 보고서를 일별로 처리), 및 [!DNL Report.cfg] 파일 설정.

보고서를 생성하는 동안 완료율이 [!DNL Reports] 해당 특정 보고서의 축소판 아래에 있는 탭입니다. If [!DNL Report] 보고서 생성 중에 문제가 발생하면 가장 최근 오류 메시지가 [!DNL Reports] 보고서 세트의 폴더에 있는 탭입니다. If [!DNL Report] 은 특정 보고서에 대한 오류가 발생하면 집합의 다른 보고서를 계속 처리합니다.

보고서 세트의 보고서를 [!DNL Report Types] 의 매개 변수 [!DNL Report.cfg] 파일:

* Microsoft Excel 파일( [!DNL .xls] 또는 [!DNL .xlsx])
* 휴대용 네트워크 그래픽 파일( [!DNL .png])
* 축소판 그림 ( [!DNL .jpg])

지정한 출력 유형과 함께 [!DNL Report] 만들기 [!DNL .xml] 파일의 이름은 보고서와 동일합니다. 이 *`<report name>`*.xml 파일에는 Data Workbench에 표시되는 보고서의 설명이 들어 있습니다 [!DNL Reports] 보고서의 축소판 아래에 있는 탭입니다. 이렇게 하면 설명을 보고 포털을 통해 보고서를 배포할 때 사용할 수 있습니다. 에 대한 정보 [!DNL Report Portal]를 참조하십시오. [보고서 포털 작업](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35).

>[!NOTE]
>
>내부 지표를 재정의하는 경우 시스템이 잘못된 값 때문에 예기치 않게 동작합니다. 지표를 100% 읽지 못하면 보고서가 생성되지 않습니다. 지표 정의를 변경하지 않는 것이 좋습니다.
