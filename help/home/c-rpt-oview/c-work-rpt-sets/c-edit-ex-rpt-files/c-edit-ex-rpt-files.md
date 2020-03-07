---
description: 작업상이나 텍스트 편집기를 사용하여 기존 Report.cfg 파일을 편집하는 절차.
solution: Analytics
title: 기존 Report.cfg 파일 편집
topic: Data workbench
uuid: 494b9eef-42f3-4ed9-8b43-f5c09af33f2e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 기존 Report.cfg 파일 편집{#editing-existing-report-cfg-files}

작업상이나 텍스트 편집기를 사용하여 기존 Report.cfg 파일을 편집하는 절차.

>[!NOTE]
>
>* 온라인으로 [!DNL Report.cfg] 파일을 편집해야 합니다. 온라인으로 작업하려면 제목 표시줄에서 [!DNL Worktop]마우스 오른쪽 버튼을 클릭한 다음 을 클릭합니다 **[!UICONTROL Work Online]**.
   >
   >
* 파일의 **[!UICONTROL Allow Report Regeneration]** 매개 변수가 로 설정된 [!DNL Report.cfg] 경우 해당 파일을 변경하고 해당 파일을 다시 서버에 저장하면 해당 세트에 있는 보고서가 [!DNL True][!DNL Report] 자동으로 다시 생성됩니다. 보고서를 다시 생성하지만 이메일로 보고서를 다시 전송하지는 않습니다. 이를 위한 단계는 이메일로 보고서 [재전송을 참조하십시오](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/t-res-rpts-email.md#task-b0a21f1c925f4e5d82560581ae4cf607).
>



텍스트 편집기를 사용하거나 [!DNL Report.cfg] 에서 기존 [!DNL Worktop] 텍스트를 편집할 수 있습니다.

의 [!DNL Report.cfg] 탭을 사용하여 [!DNL Reports] 파일을 편집하면 [!DNL Worktop] 파일에 이미 존재하는 매개 변수, 벡터 및 벡터 항목만 편집할 수 있습니다. 파일에 매개 변수 또는 벡터를 추가해야 하는 경우 메모장과 같은 텍스트 편집기를 사용하여 매개 변수를 편집해야 합니다.

* [작업대를 사용하여 기존 Report.cfg를 편집하려면](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-7bce3bca006149c79be7678430f21945)
* [텍스트 편집기를 사용하여 기존 Report.cfg를 편집하려면](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-06f3d2a8d7f34bc2841180caf10a1eb7)

## 작업대를 사용하여 기존 Report.cfg를 편집하려면 {#section-7bce3bca006149c79be7678430f21945}

>[!NOTE]
>
>Adobe Connect Central Enterprise Edition을 사용하려면 온라인 작업 중에 있어야 [!DNL Report.cfg] 합니다 [!DNL Worktop].

1. 데이터 워크벤치의 [!DNL Reports] 탭에서 구성할 보고서 세트에 대한 하위 폴더(탭 또는 드롭다운 하위 디렉토리)를 선택합니다.
1. 클릭 **[!UICONTROL Report.cfg]**. 이 보고서 세트에 대한 매개 변수가 [!DNL Report.cfg] 표시됩니다.

1. 원하는 대로 구성 매개 변수를 편집합니다. 이러한 매개 변수에 대한 자세한 내용은 Report.cfg [매개 변수를 참조하십시오](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. 매개 변수 맨 위에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Report.cfg (modified)]** &lt; **[!UICONTROL Save to]***> **[!UICONTROL server location]***을 클릭하여 파일을 저장합니다.

## 텍스트 편집기를 사용하여 기존 Report.cfg를 편집하려면 {#section-06f3d2a8d7f34bc2841180caf10a1eb7}

1. 작업 영역 내에서 마우스 오른쪽 단추를 [!DNL Reports Manager] 클릭하고 **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Reports Manager]**&#x200B;를 클릭하여 을 엽니다.

1. 보고서 세트의 폴더를 클릭합니다.
1. 이 보고서 세트 옆에 [!DNL Report.cfg] 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다.

1. 열에서 이 보고서 세트 옆에 [!DNL User] 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Report.cfg] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다. 파일이 [!DNL Report.cfg] 열립니다.

   보고서 세트 [!DNL Report.cfg] 구성에 [표시된 샘플에는](../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0) 기본적으로 파일에 포함된 [!DNL Report.cfg] 매개 변수만 포함되어 있습니다. 다음 예에는 매개변수 항목에 대해 모델로 사용할 수 있는 [!DNL Report.cfg] 파일에 사용할 수 있는 모든 매개변수가 포함되어 있습니다.

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

1. 원하는 대로 구성 매개 변수를 편집합니다. 이러한 매개 변수에 대한 자세한 내용은 Report.cfg [매개 변수를 참조하십시오](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. 파일을 저장하고 닫습니다.
1. 에서 [!DNL Reports Manager]파일의 [!DNL User] 열에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Report.cfg] &lt; **[!UICONTROL Save to]***> **[!UICONTROL profile name]***를 선택합니다.

