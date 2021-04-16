---
description: 보고서 세트 폴더 내의 작업 영역을 만들고 저장한 후에는 새 Report.cfg 파일을 만들어야 합니다.
title: 보고서 세트 구성
uuid: 21f8dcde-8fe1-4ba0-9eb7-39ff812dcf14
exl-id: 780e6bb1-b332-4984-b132-df11d95b592a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 4%

---

# 보고서 세트 구성{#configure-the-report-set}

보고서 세트 폴더 내의 작업 영역을 만들고 저장한 후에는 새 Report.cfg 파일을 만들어야 합니다.

보고서를 생성하고 배포할 시기와 방법을 보고서 세트에 대해 [!DNL Report.cfg] 파일에 지정해야 합니다.

**새 Report.cfg를 만들려면**

1. 데이터 워크벤치에서 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Profile Manager]**&#x200B;를 클릭하여 [!DNL Profile Manager]을(를) 엽니다.
1. **[!UICONTROL Reports]**&#x200B;을 클릭하여 [!DNL Reports] 폴더를 엽니다.
1. 보고서 세트에 대한 폴더를 클릭합니다.
1. 보고서 세트 폴더의 [!DNL User] 열에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Create]** > **[!UICONTROL Report]**&#x200B;를 선택합니다. 새 [!DNL Report.cfg] 파일이 [!DNL File]열에 나타납니다.
1. 새 [!DNL Report.cfg] 파일의 [!DNL User] 열에서 [!DNL Report.cfg] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다.

   ![단계 정보](assets/cfg_reportcfg.png)

1. 원하는 대로 구성 매개 변수를 편집합니다. 이러한 매개 변수에 대한 자세한 내용은 [Report.cfg 매개 변수](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff)를 참조하십시오.

   >[!NOTE]
   >
   >이 예제에 표시된 샘플 [!DNL Report.cfg]에는 기본적으로 [!DNL Report.cfg] 파일에 포함된 매개 변수만 포함되어 있습니다. [!DNL Report.cfg] 파일에 매개 변수를 더 추가해야 하는 경우에는 텍스트 편집기를 사용하여 매개 변수를 추가해야 합니다. 이 작업을 수행하려면 [기존 Report.cfg 파일 편집](../../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887)을 참조하십시오.

1. 파일 맨 위에서 **[!UICONTROL Report.cfg (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save as Reports\]***&lt; **[!UICONTROL ReportSetName]*****[!UICONTROL \Report.cfg]**를 클릭하여 파일을 저장합니다.
1. 파일을 닫습니다.
1. [!DNL Profile Manager]에서 새 [!DNL Report.cfg] 파일의 [!DNL User] 열에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]***&lt; **[!UICONTROL profile name]***를 선택합니다.
