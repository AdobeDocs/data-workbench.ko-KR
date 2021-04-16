---
description: 작업상이나 텍스트 편집기를 사용하여 기존 Report.cfg 파일을 편집하는 절차.
title: 기존 Report.cfg 파일 편집
uuid: 494b9eef-42f3-4ed9-8b43-f5c09af33f2e
exl-id: 69038c0c-bb01-4e61-aad6-1be0bdec8a6d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 2%

---

# 기존 Report.cfg 파일 편집{#editing-existing-report-cfg-files}

작업상이나 텍스트 편집기를 사용하여 기존 Report.cfg 파일을 편집하는 절차.

>[!NOTE]
>
>* [!DNL Report.cfg] 파일을 편집하려면 온라인으로 작업해야 합니다. 온라인으로 작업하려면 [!DNL Worktop]에서 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]**&#x200B;을 클릭합니다.
   >
   >
* [!DNL Report.cfg] 파일의 **[!UICONTROL Allow Report Regeneration]** 매개 변수가 [!DNL True]로 설정된 경우 해당 파일을 변경하고 다시 서버에 저장하면 [!DNL Report]은 해당 세트에 있는 보고서를 자동으로 다시 생성합니다. 보고서를 다시 생성하지만 이메일로 보고서를 다시 전송하지는 않습니다. 그렇게 하는 단계는 [이메일로 보고서 다시 전송을 참조하십시오](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/t-res-rpts-email.md#task-b0a21f1c925f4e5d82560581ae4cf607).

>



[!DNL Worktop] 또는 텍스트 편집기를 사용하여 기존 [!DNL Report.cfg]을 편집할 수 있습니다.

[!DNL Worktop]의 [!DNL Reports] 탭을 사용하여 [!DNL Report.cfg] 파일을 편집하면 이미 파일에 있는 매개 변수, 벡터 및 벡터 항목만 편집할 수 있습니다. 매개 변수 또는 벡터를 파일에 추가해야 하는 경우 메모장과 같은 텍스트 편집기를 사용하여 매개 변수를 편집해야 합니다.

* [작업대를 사용하여 기존 Report.cfg를 편집하려면](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-7bce3bca006149c79be7678430f21945)
* [텍스트 편집기를 사용하여 기존 Report.cfg를 편집하려면](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-06f3d2a8d7f34bc2841180caf10a1eb7)

## 작업톱 {#section-7bce3bca006149c79be7678430f21945}을 사용하여 기존 Report.cfg를 편집하려면

>[!NOTE]
>
>[!DNL Worktop]에서 [!DNL Report.cfg]을(를) 편집하려면 온라인상에서 작업해야 합니다.

1. 데이터 워크벤치의 [!DNL Reports] 탭에서 구성할 보고서 세트에 대한 하위 폴더(탭 또는 드롭다운 하위 디렉토리)를 선택합니다.
1. 클릭 **[!UICONTROL Report.cfg]**. 이 보고서 세트에 대한 [!DNL Report.cfg]의 매개 변수가 표시됩니다.

1. 원하는 대로 구성 매개 변수를 편집합니다. 이러한 매개 변수에 대한 자세한 내용은 [Report.cfg 매개 변수](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff)를 참조하십시오.
1. 매개 변수의 맨 위에서 **[!UICONTROL Report.cfg (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]***&lt; **[!UICONTROL server location]***을 클릭하여 파일을 저장합니다.

## 텍스트 편집기 {#section-06f3d2a8d7f34bc2841180caf10a1eb7}를 사용하여 기존 Report.cfg를 편집하려면

1. 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Reports Manager]**&#x200B;을 클릭하여 [!DNL Reports Manager]을 엽니다.

1. 보고서 세트에 대한 폴더를 클릭합니다.
1. 이 보고서 세트에 대해 [!DNL Report.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 을 클릭합니다.

1. [!DNL User] 열에서 이 보고서 세트에 대한 [!DNL Report.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다. [!DNL Report.cfg] 파일이 열립니다.

   [보고서 세트 구성](../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0)에 표시된 샘플 [!DNL Report.cfg]에는 기본적으로 [!DNL Report.cfg] 파일에 포함된 매개 변수만 포함되어 있습니다. 다음 예제에서는 매개 변수 항목에 대한 모델로 사용할 수 있는 [!DNL Report.cfg] 파일에 사용할 수 있는 모든 매개 변수를 포함합니다.

   ```
   Attachments = vector: 1 items
     0 = Attachment:
       FileName = string: c:\\myimage.jpg
       Content Type = string: image/jpeg
   Alert Threshold = int: 0
   Allow Report Regeneration = bool: true
   Color Set = int: 1
   Command To Execute = string: 
   Default Excel Template = string: 
   Dimension Name = string: 
   Email Only If Perfect = bool: false
   End Date = string: 
   Every = string: month
   Excel Watchdog Timeout (seconds) = double: 300.0
   Filter Formula = string: 
   Gamma Correction = double: 1
   Hide Logos = bool: false
   Lookup File = string: 
   Mail Report = MailReport: 
     Body XSL Template = string: 
     Recipients = vector: 0 items
     SMTP Server = SmtpServerInfo: 
       Address = string: 
       Password = string: 
       User = string: 
     Sender Address = string: 
     Sender Name = string: 
     Subject = string: 
   Notification Only = bool: false
   Output Root = string: 
   Report Types = vector: 3 items
     0 = string: thumbnail
     1 = string: png
     2 = string: excel
   Start Date = string: 7/1/06 19:16 EDT
   Thumbnail X = int: 240
   Thumbnail Y = int: 180
   Top N Metric = string: 
   Top N Value = int: 0
   Use Local Sample Only = bool: false
   Workspace Path = string: 
   ```

1. 원하는 대로 구성 매개 변수를 편집합니다. 이러한 매개 변수에 대한 자세한 내용은 [Report.cfg 매개 변수](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff)를 참조하십시오.
1. 파일을 저장하고 닫습니다.
1. [!DNL Reports Manager]에서 [!DNL Report.cfg] 파일의 [!DNL User] 열에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]***&lt; **[!UICONTROL profile name]***를 선택합니다.
