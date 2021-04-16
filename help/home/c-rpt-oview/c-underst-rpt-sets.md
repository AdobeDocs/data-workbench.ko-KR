---
description: 보고서 세트는 보고서 서버가 Report.cfg 구성 파일에 지정된 값을 기반으로 생성하는 작업 영역 모음입니다.
title: 보고서 세트 이해
uuid: 421055d7-0cf0-4664-b944-327a254a97a4
exl-id: 95609a1a-e70c-41e2-ace3-0cb09f77705a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# 보고서 세트 이해{#understanding-report-sets}

보고서 세트는 보고서 서버가 Report.cfg 구성 파일에 지정된 값을 기반으로 생성하는 작업 영역 모음입니다.

[!DNL Insight] 설치 폴더에서 &lt;*작업 프로필 이름*\Reports 폴더 내의 각 하위 폴더는 만든 보고서 세트를 나타냅니다. 각 보고서 세트에는 해당 하위 폴더 내에 고유한 [!DNL Report.cfg] 구성 파일이 있습니다.

>[!NOTE]
>
>Data Workbench의 [!DNL Profile Manager]에서 보고서 세트는 [!DNL Reports] 폴더 내의 하위 폴더로 표시됩니다. [!DNL Profile Manager]에 대한 자세한 내용은 [Data Workbench 사용 안내서](https://docs.adobe.com/content/help/en/data-workbench/using/home.html#Data_Workbench_Help)를 참조하십시오.

[!DNL Report.cfg] 파일에서 보고서 세트에 대한 특정 구성 설정을 정의하여 보고서를 받는 사람 및 어떤 형식의 보고서 세트를 포함하여 보고서의 생성 및 배포를 예약할 수 있습니다.
