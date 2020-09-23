---
description: Communications 구성 파일 Communications.cfg에는 Insight 서버 네트워크 설정과 Access Control.cfg 파일 경로가 포함됩니다.
solution: Analytics
title: 통신 구성
uuid: 04d08206-17b1-4348-a945-0c907c9a494c
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---


# 통신 구성{#configuring-communications}

Communications 구성 파일 Communications.cfg에는 Insight 서버 네트워크 설정과 Access Control.cfg 파일 경로가 포함됩니다.

이러한 설정을 통해 연결할 수 [!DNL Insight Server]있습니다.

**권장 빈도:** 필요한 경우에만

**통신 설정을 보고 수정하려면[!DNL Insight]**

1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.
1. 구성할 아이콘 [!DNL Insight Server] 을 마우스 오른쪽 단추로 클릭하고 클릭합니다 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Components]** 를 봅니다. 이 디렉터리 내에 [!DNL Communications.cfg] 파일이 있습니다.
1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 [!DNL Communications.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 열에 확인 표시가 [!DNL Temp] 나타납니다 [!DNL Communications.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** 를 **[!UICONTROL in Insight]**&#x200B;클릭합니다.
1. 창에서 [!DNL Communications.cfg] 을 클릭하여 내용 **[!UICONTROL component]** 을 봅니다.
1. 필요에 따라 설정을 변경합니다. 이 파일에서 사용할 수 있는 매개 변수에 대한 자세한 내용은 [통신 구성 설정을 참조하십시오](../../../home/c-inst-svr/c-cfg-stgs-ref/c-comm-cfg-stgs.md#concept-aed00587c7a1432fb487bd154aaea6b1).

   ![단계 정보](assets/cfg_communications_examplevalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 위쪽 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 열 [!DNL Server Files Manager]에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 선택합니다&#x200B;**[!UICONTROL server name]***.

