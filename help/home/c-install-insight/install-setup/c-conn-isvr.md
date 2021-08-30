---
description: Insight 소프트웨어 및 디지털 인증서를 설치한 후에는 Insight를 시작하고 Insight Server에 연결을 구성해야 합니다.
title: Insight Server에 연결 구성
uuid: 8ba13da6-8749-49fe-a29e-dac3906f71b8
exl-id: 6a87e972-069a-435c-9bac-23b20f165ebb
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 1%

---

# Insight Server에 연결 구성{#configuring-the-connection-to-insight-server}

Insight 소프트웨어 및 디지털 인증서를 설치한 후에는 Insight를 시작하고 Insight Server에 연결을 구성해야 합니다.

>[!NOTE]
>
>경우에 따라 Insight Server에 대한 연결이 Adobe 컨설팅 서비스 또는 시스템 관리자가 미리 구성했을 수 있습니다. 그런 경우에는 이 작업을 완료할 필요가 없습니다.

Insight를 처음 시작하면 디지털 인증서를 등록하기 위해 Adobe 라이선스 서버에 자동으로 연결됩니다. 등록 프로세스를 성공적으로 완료하려면 다음 단계를 실행할 때 컴퓨터가 인터넷에 연결되어 있어야 합니다.

>[!NOTE]
>
>[디지털 인증서 다운로드 및 설치에서 설명한 대로 미리 잠금 인증서를 요청, 다운로드 및 설치한 경우, Insight는 라이센스 서버에 연결을 시도하지 않으며 오류가 표시되지 않습니다.](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#topic-fed3b44e472c4e4ca6dd5852af14cdb9)

**Insight Server에 연결을 구성하려면**

클러스터된 환경에서 작업할 경우 동기화 문제를 방지하기 위해 Insight를 마스터 Insight Server에 액세스하도록 구성해야 합니다. Insight에서는 [서버 관리자](https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/c-svrs-mgr.html)의 [!DNL Related Servers] 메뉴 항목을 사용하여 클러스터에서 처리 [!DNL Insight Servers]에 대한 정보를 볼 수 있습니다.

1. Insight를 시작합니다.
1. [!DNL Worktop]에서 **[!UICONTROL Admin]**, **[!UICONTROL First Steps]** 를 차례로 클릭합니다.

1. **[!UICONTROL Configure Connection to Servers]** 축소판을 클릭합니다.

   [!DNL Servers Manager], [!DNL Insight.cfg] 파일 및 [!DNL Insight.cfg]파일 구성에 대한 지침이 표시됩니다.

1. [!DNL Insight.cfg] 창에서 **[!UICONTROL Servers]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new child]** > **[!UICONTROL Server]** 를 클릭합니다.

   ![](assets/cfg_Workstation_AddChild.png)

1. 서버 매개 변수를 완료하거나 수정하여 Insight Server에 대한 액세스 권한을 Insight에 제공합니다. Insight.cfg 파일에 있는 매개 변수에 대한 자세한 설명은 [구성 매개 변수](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-insght-config-param.html)를 참조하십시오.

   ![](assets/cfg_Workstation_AddServer.png)

1. 연결을 구성할 각 Insight Server에 대해 4단계 및 5단계를 반복합니다.
1. 구성 변경 사항을 저장하려면 창 상단에서 **[!UICONTROL Insight.cfg (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save as Insight.cfg]** 를 클릭합니다.

   Insight는 지정한 설정을 사용하여 [!DNL Insight Server(s)]에 연결을 시도합니다. 연결이 설정되면 다음 페이지에 표시된 대로 [!DNL Servers Manager]에 녹색 노드가 나타납니다.

   ![](assets/vis_SysStat_RedGreenDots.png)

   * **녹색:**  Insight Server에 대한 연결이 활성화되어 있음을 나타냅니다.
   * **빨간색 조명:**  서버 처리 중인 드레인, 높은 메모리 사용 또는 낮은 디스크 공간과 같이 서버에 발생할 수 있는 문제를 나타냅니다.
   * **빨간색:** Insight Server에 대한 연결이 활성화되어 있지 않음을 나타냅니다.

   Insight가 지정된 설정을 사용하여 연결할 수 없는 경우 [!DNL Servers Manager]에 빨간색 노드가 나타납니다. 이 경우 [연결 문제 해결](../../../home/c-install-insight/install-setup/t-conn-trbsh.md#task-034e588c5ce04c4a8f6d0097364d3b2b)을 참조하십시오.

<!--
c_dir_crt_setup.xml
-->

사용할 프로필을 선택하면 프로필 정보(관련 데이터 및 프로필에 대해 정의된 특정 작업 공간 또는 시각화 포함)가 컴퓨터에 다운로드됩니다. 각 프로필을 다운로드할 때 Insight는 프로필 이름을 사용하여 설치 디렉토리 내에 폴더를 만듭니다.

예를 들어, Sales라는 프로필을 선택하면 Insight 디렉토리에 Sales 폴더가 표시됩니다. 이 폴더에는 Sales 프로필에 정의된 지표, 차원, 작업 공간 및 시각화가 들어 있습니다. 프로필을 처음 로드한 후 오프라인에서 작업할 때 프로필을 사용할 수 있습니다. [오프라인 및 온라인 작업](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-off-on.html)을 참조하십시오.

또한 Insight Server에서 처음으로 Insight Server에 연결하면 Insight Server에서 Insight Installation 디렉토리에 다음 디렉토리를 만듭니다.

* **[!DNL Trace]directory:** 디렉토리  [!DNL Trace] 내에 Insight 로그 파일(  [!DNL insight.log])이 있습니다. [!DNL Insight.log] 파일의 크기가 100MB에 도달하면 파일의 이름이 [!DNL insight-1.log]로 변경됩니다. 이름 [!DNL insight-1.log] 의 파일이 이미 있으면 [!DNL insight-1.log] 이름이 [!DNL insight-2.log](으)로 변경되고 최대값 [!DNL insight-9.log]이 사용됩니다. [!DNL insight.log] 파일에는 항상 최신 로그 정보가 포함되며 [!DNL insight-max.log]에는 가장 오래된 로그 정보가 포함됩니다.

* **[!DNL User]디렉토리:** 디렉토리 내 [!DNL User] 에 있는 폴더는 날짜에 사용된 각 프로필에 해당하는 폴더이며, 각 프로필 폴더 내에서는  [!DNL Work] 및  [!DNL Workspaces]라는 폴더가 있습니다. `User\*profile name*\Workspaces` 디렉토리는 Insight 작업 공간 파일이 저장되는 기본 위치입니다. `User\*profile name*\Work` 인사이트 사용자가 수행한 인사이트 시각화 및 기타 사용자 지정 작업이 저장되는 기본 위치입니다.

다음 표에는 자주 액세스하는 구성 요소의 기본 위치가 나열되어 있습니다.

<table id="table_0254A8C25AF5400F89F87A242746D07E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 구성 요소 </th> 
   <th colname="col2" class="entry"> 디렉토리 위치 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>저장된 시각화 </p> </td> 
   <td colname="col2"> <p><i>Insight</i>\User\<i>프로필 이름</i>\Work\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> 작업 공간이 저장됨</span> </p> </td> 
   <td colname="col2"> <p><i>Insight</i>\User\<i>프로필 이름</i>\Workspaces\<i>탭 이름</i>\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>저장한<span class="filepath">.png</span> 파일 </p> </td> 
   <td colname="col2"> <p><i>Insight</i>\User\<i>프로필 이름</i>\Work\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>데이터 캐시 </p> </td> 
   <td colname="col2"> <p><i>인사이트</i>\User\Cache.db </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="filepath"> Insight.</span> logfile </p> </td> 
   <td colname="col2"> <p><i>인사이트</i>\Trace\ </p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
c_config_file_ent.xml
-->

키 이름, 키 유형 또는 값으로 검색하여 항목을 빠르게 찾고, 중첩된 정보를 위해 확장되고 큰 파일을 스크롤해야 하는 번거로움을 제거할 수 있습니다. 차원 이름, 서버 이름 등을 찾을 수 있습니다. 다음 예제는 구문 맵의 검색에 대한 일치를 보여줍니다.

![](assets/cfg_search.PNG)

이 필드에 검색 구문을 입력하여 데이터를 찾습니다. 일치의 성공에 따라 필드 색상이 변경됩니다. 일치하는 항목이 강조 표시되고 일치하지 않는 항목은 흐리게 표시됩니다. 일치하는 항목이 없으면 검색 필드의 배경이 빨간색으로 표시됩니다. Enter 키를 누르면 구성 트리가 일치하는 모든 위치에 확장되며 일치하는 항목이 없는 경우 축소됩니다.

[!DNL Search] 필드에서도 정규 표현식을 사용할 수 있습니다. 예를 들어 다음 항목을 사용할 수 있습니다. [!DNL *zip*] &quot;zip&quot;이라는 단어를 포함하는 모든 항목에 대해

검색을 지우려면 **[!UICONTROL Escape]** 키를 누릅니다.
