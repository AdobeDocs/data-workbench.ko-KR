---
description: 보고서를 이메일로 다시 보내는 절차.
title: 이메일로 보고서 다시 보내기
uuid: 384dfa1f-6a72-4fef-886e-bf2290f5993f
exl-id: eb37fd3e-6e7b-4672-bcf0-fffa9f10997d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 6%

---

# 이메일로 보고서 다시 보내기{#resending-reports-by-email}

{{eol}}

보고서를 이메일로 다시 보내는 절차.

만약 **[!UICONTROL Allow Report Regeneration]** 의 매개 변수 [!DNL Report.cfg] 파일이 [!DNL True]를 변경하는 경우 [!DNL Report.cfg] 파일을 다시 서버로 저장하면 보고서 서버가 해당 세트에 있는 보고서를 자동으로 다시 생성합니다. 보고서를 이메일로 다시 전송하지 않습니다.

1. 설정 [!DNL Reports] 탭에서 재연결할 보고서 세트의 하위 폴더(탭 또는 드롭다운 하위 디렉토리)를 선택합니다.
1. 클릭 **[!UICONTROL Report.cfg]**. 의 매개 변수 [!DNL Report.cfg] 이 보고서 세트에 대해 가 표시됩니다.
1. 변경 **[!UICONTROL Start Date]** 매개 변수를 사용하십시오.
1. 마우스 오른쪽 단추를 클릭하여 파일을 저장합니다 **[!UICONTROL Report.cfg (modified)]** 매개 변수 맨 위에서 을(를) 클릭하고 **[!UICONTROL Save to]***&lt; **[!UICONTROL server location]**>*.
이 세트의 보고서가 다시 생성되며 지정된 수신자에게 이메일로 다시 전송됩니다.
