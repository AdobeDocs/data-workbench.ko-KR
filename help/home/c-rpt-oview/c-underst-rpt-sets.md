---
description: 보고서 세트는 Report.cfg 구성 파일에 지정된 값을 기반으로 보고서 서버가 생성하는 작업 공간의 컬렉션입니다.
title: 보고서 세트 이해
uuid: 421055d7-0cf0-4664-b944-327a254a97a4
exl-id: 95609a1a-e70c-41e2-ace3-0cb09f77705a
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---

# 보고서 세트 이해{#understanding-report-sets}

보고서 세트는 Report.cfg 구성 파일에 지정된 값을 기반으로 보고서 서버가 생성하는 작업 공간의 컬렉션입니다.

[!DNL Insight] 설치 폴더에서 &lt;*작업 프로필 이름*\Reports 폴더 내의 각 하위 폴더는 생성된 보고서 세트를 나타냅니다. 각 보고서 세트에는 해당 하위 폴더 내에 고유한 [!DNL Report.cfg] 구성 파일이 있습니다.

>[!NOTE]
>
>Data Workbench의 [!DNL Profile Manager]에서 보고서 세트는 [!DNL Reports] 폴더 내에 하위 폴더로 나타납니다. [!DNL Profile Manager]에 대한 자세한 내용은 [Data Workbench 사용 안내서](https://experienceleague.adobe.com/docs/data-workbench/using/home.html#Data_Workbench_Help)를 참조하십시오.

보고서 세트의 [!DNL Report.cfg] 파일에 있는 보고서 세트에 대한 특정 구성 설정을 정의하면 누가 어떤 보고서를 받고 어떤 형식으로 보고서 세트를 만드는지 등 보고서의 생성 및 배포를 예약할 수 있습니다.
