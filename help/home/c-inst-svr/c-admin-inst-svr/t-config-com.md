---
description: Communications.cfg의 Communications 구성 파일에는 Insight Server 네트워크 설정과 Access Control.cfg 파일의 경로가 포함되어 있습니다.
solution: Insight
title: 통신 구성
uuid: 04d08206-17b1-4348-a945-0c907c9a494c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 통신 구성{#configuring-communications}

Communications.cfg의 Communications 구성 파일에는 Insight Server 네트워크 설정과 Access Control.cfg 파일의 경로가 포함되어 있습니다.

이러한 설정을 사용하면 연결할 수 [!DNL Insight Server]있습니다.

**권장 빈도:** 필요한 경우에만

**통신 설정을 보고 수정하려면[!DNL Insight]**

1. &#x200B;> [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 구성할 아이콘 을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Communications.cfg] 파일은 이 디렉토리 내에 있습니다.
1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Communications.cfg] **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Communications.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Insight]**&#x200B;을 클릭합니다.
1. 창에서 [!DNL Communications.cfg] 을 클릭하여 내용을 **[!UICONTROL component]** 봅니다.
1. 필요에 따라 설정을 변경합니다. 이 파일에서 사용할 수 있는 매개 변수에 대한 자세한 내용은 통신 구성 [설정을 참조하십시오](../../../home/c-inst-svr/c-cfg-stgs-ref/c-comm-cfg-stgs.md#concept-aed00587c7a1432fb487bd154aaea6b1).

   ![단계 정보](assets/cfg_communications_examplevalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *를 선택합니다&#x200B;**[!UICONTROL server name]***.

