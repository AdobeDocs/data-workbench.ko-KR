---
description: Communications 구성 파일 Communications.cfg에는 Insight Server 네트워크 설정과 Access Control.cfg 파일의 경로가 포함됩니다.
title: 통신 구성
uuid: 04d08206-17b1-4348-a945-0c907c9a494c
exl-id: af5e788e-8904-4c68-b02a-c95b523b076d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---

# 통신 구성{#configuring-communications}

{{eol}}

Communications 구성 파일 Communications.cfg에는 Insight Server 네트워크 설정과 Access Control.cfg 파일의 경로가 포함됩니다.

이러한 설정은 [!DNL Insight Server].

**권장 빈도:** 필요한 경우에만

**에서 통신 설정을 보고 수정하려면[!DNL Insight]**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.
1. 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 구성하고 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Communications.cfg] 파일이 이 디렉터리 내에 있습니다.
1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 [!DNL Communications.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Communications.cfg].
1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. 에서 [!DNL Communications.cfg] 창 **[!UICONTROL component]** 콘텐츠를 보려면 클릭하십시오.
1. 필요에 따라 설정을 변경합니다. 이 파일에서 사용할 수 있는 매개 변수에 대한 자세한 내용은 [통신 구성 설정](../../../home/c-inst-svr/c-cfg-stgs-ref/c-comm-cfg-stgs.md#concept-aed00587c7a1432fb487bd154aaea6b1).

   ![단계 정보](assets/cfg_communications_examplevalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 선택 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
