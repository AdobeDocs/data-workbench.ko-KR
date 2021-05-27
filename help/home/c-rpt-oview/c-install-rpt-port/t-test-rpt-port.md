---
description: 보고서 포털을 열고 프로필에 대한 보고서를 성공적으로 볼 수 있는지 확인하는 단계입니다.
title: 보고서 포털 테스트
uuid: eee0df5e-78e0-49b2-853c-40f1b332328b
exl-id: 197ff815-9234-4dce-b30f-b9cacf259634
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---

# 보고서 포털 테스트{#test-the-report-portal}

보고서 포털을 열고 프로필에 대한 보고서를 성공적으로 볼 수 있는지 확인하는 단계입니다.

>[!NOTE]
>
>보고서가 출력 폴더에 나타날 때까지 [!DNL Report Portal]에 로그인할 수 없습니다.

1. 웹 브라우저에서 다음 URI 형식을 사용하여 [!DNL Report Portal] 을 엽니다.

   http://*ServerAddress*/*PortalName*

   예: [!DNL http://localhost/VisualReportPortal]

1. 로그인 자격 증명을 입력하라는 메시지가 [!DNL Report Portal]에 표시되면 계정 이름과 암호를 입력합니다(예: 기본 계정의 계정 &quot;test&quot; 및 암호 &quot;user&quot;).
1. [!DNL Report Portal] 이 나타나면 다음을 확인합니다.

   * 포털에는 출력 폴더에 있는 각 보고서 세트에 대한 탭이 포함되어 있습니다.
   * 각 탭에는 보고서 세트의 요약 보고서가 표시됩니다.
   * 각 탭의 메뉴에는 보고서 세트에 대한 개별 하위 폴더(있는 경우)가 나열되고 해당 폴더의 내용이 표시됩니다.
