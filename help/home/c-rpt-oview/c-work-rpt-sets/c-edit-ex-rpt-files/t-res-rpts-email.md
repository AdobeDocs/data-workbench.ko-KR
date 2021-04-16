---
description: 보고서를 이메일로 다시 보내는 절차.
title: 이메일로 보고서 다시 보내기
uuid: 384dfa1f-6a72-4fef-886e-bf2290f5993f
exl-id: eb37fd3e-6e7b-4672-bcf0-fffa9f10997d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 6%

---

# 이메일로 보고서 다시 보내기{#resending-reports-by-email}

보고서를 이메일로 다시 보내는 절차.

[!DNL Report.cfg] 파일의 **[!UICONTROL Allow Report Regeneration]** 매개 변수가 [!DNL True]로 설정된 경우 [!DNL Report.cfg] 파일을 변경하고 다시 서버에 저장하면 보고서 서버가 자동으로 해당 세트의 보고서를 다시 생성합니다. 이메일로 보고서를 다시 보내지 않습니다.

1. [!DNL Reports] 탭에서 재전송하려는 보고서 세트에 대한 하위 폴더(탭 또는 드롭다운 하위 디렉토리)를 선택합니다.
1. 클릭 **[!UICONTROL Report.cfg]**. 이 보고서 세트에 대한 [!DNL Report.cfg]의 매개 변수가 표시됩니다.
1. **[!UICONTROL Start Date]** 매개 변수를 보고서를 재전송할 미래 시간으로 변경합니다.
1. 매개 변수의 맨 위에서 **[!UICONTROL Report.cfg (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]***&lt; **[!UICONTROL server location]***을 클릭하여 파일을 저장합니다.
이 세트의 보고서가 다시 생성되며 지정된 수신자에게 이메일로 다시 전송됩니다.
