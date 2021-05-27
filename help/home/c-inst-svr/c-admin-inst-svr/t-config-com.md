---
description: Communications 구성 파일 Communications.cfg에는 Insight Server 네트워크 설정과 Access Control.cfg 파일의 경로가 포함됩니다.
title: 통신 구성
uuid: 04d08206-17b1-4348-a945-0c907c9a494c
exl-id: af5e788e-8904-4c68-b02a-c95b523b076d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---

# 통신 구성{#configuring-communications}

Communications 구성 파일 Communications.cfg에는 Insight Server 네트워크 설정과 Access Control.cfg 파일의 경로가 포함됩니다.

이러한 설정은 [!DNL Insight Server]에 연결하는 데 도움이 됩니다.

**권장 빈도:**  필요한 경우에만

**에서 통신 설정을 보고 수정하려면[!DNL Insight]**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.
1. 구성할 [!DNL Insight Server] 아이콘을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.
1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 해당 콘텐츠를 봅니다. [!DNL Communications.cfg] 파일이 이 디렉터리 내에 있습니다.
1. [!DNL Communications.cfg]에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;를 클릭합니다. [!DNL Communications.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.
1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다.
1. [!DNL Communications.cfg] 창에서 **[!UICONTROL component]** 을 클릭하여 해당 콘텐츠를 봅니다.
1. 필요에 따라 설정을 변경합니다. 이 파일에서 사용할 수 있는 매개 변수에 대한 자세한 내용은 [통신 구성 설정](../../../home/c-inst-svr/c-cfg-stgs-ref/c-comm-cfg-stgs.md#concept-aed00587c7a1432fb487bd154aaea6b1)을 참조하십시오.

   ![단계 정보](assets/cfg_communications_examplevalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 선택합니다.
