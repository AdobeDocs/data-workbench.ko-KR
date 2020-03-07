---
description: 보고서를 이메일로 다시 보내는 절차.
solution: Analytics
title: 이메일로 보고서 다시 보내기
topic: Data workbench
uuid: 384dfa1f-6a72-4fef-886e-bf2290f5993f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 이메일로 보고서 다시 보내기{#resending-reports-by-email}

보고서를 이메일로 다시 보내는 절차.

파일의 매개 변수가 로 설정된 **[!UICONTROL Allow Report Regeneration]** 경우 [!DNL Report.cfg] [!DNL True][!DNL Report.cfg] 파일을 변경하고 해당 파일을 다시 서버에 저장하면 보고서 서버가 해당 세트에 있는 보고서를 자동으로 다시 생성합니다. 보고서를 이메일로 다시 보내지 않습니다.

1. 탭에서 재전송하려는 보고서 세트의 하위 폴더(탭 또는 드롭다운 하위 디렉터리)를 선택합니다. [!DNL Reports]
1. 클릭 **[!UICONTROL Report.cfg]**. 이 보고서 세트에 대한 매개 변수가 [!DNL Report.cfg] 표시됩니다.
1. 보고서를 재전송할 미래 시간으로 **[!UICONTROL Start Date]** 매개 변수를 변경합니다.
1. 매개 변수 맨 위에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Report.cfg (modified)]** &lt; **[!UICONTROL Save to]***> **[!UICONTROL server location]***을 클릭하여 파일을 저장합니다.
이 세트의 보고서가 다시 생성되어 지정된 수신자에게 이메일로 다시 전송됩니다.
