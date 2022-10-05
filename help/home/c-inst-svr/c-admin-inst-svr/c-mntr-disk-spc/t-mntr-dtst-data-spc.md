---
description: 데이터 집합 데이터 저장소를 위한 데이터 집합 모니터링 및 새 위치 추가에 대한 정보입니다.
title: 데이터 세트 데이터 공간 모니터링
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
exl-id: eb34d5fe-73c6-461f-8bb0-85833d8f824f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---

# 데이터 세트 데이터 공간 모니터링{#monitoring-dataset-data-space}

{{eol}}

데이터 집합 데이터 저장소를 위한 데이터 집합 모니터링 및 새 위치 추가에 대한 정보입니다.

**권장 빈도:** 5-10분마다

기본적으로 [!DNL Insight Server] 데이터 세트에 쓰기 [!DNL temp.db] 파일과 동일한 드라이브에 있는 파일 [!DNL Insight Server] 데이터 처리 장치의 프로그램 파일입니다. 데이터 집합 데이터의 양 [!DNL Insight Server] 시스템은 다음 중 먼저 발생하는 것으로 제한됩니다.

* 해당 데이터 세트에 입력된 데이터 레코드는 5억 개(5억 개)입니다
* 데이터 세트 데이터 저장 500GB
* 하나의 루트 수준 차원당 1MB의 데이터 세트 데이터가 저장됩니다(예: 방문자당 평균 200바이트의 5,000개의 레코드)

원한다면 [!DNL Insight Server] 데이터 세트를 다른 드라이브에서 유지 관리하거나 수집할 데이터의 양이 여러 드라이브를 사용해야 하는 경우 디스크 파일 구성 파일( [!DNL Disk Files.cfg])을 클릭하여 원하는 위치를 지정합니다 [!DNL Insight Server] 쓰기 [!DNL temp.db] 파일. 다음 [!DNL Disk Files.cfg] 파일은 디스크 파일(문자열 벡터)을 나열하고 [!DNL Insight Server] 재처리 및 작업 중에 실제 드라이브당 파일이 한 개 있습니다.

>[!NOTE]
>
>의 컨텐트 [!DNL Disk Files.cfg] 파일을 설치하는 동안 수정할 수 있습니다. [!DNL Insight Server]. 자세한 내용은 [데이터 집합 위치 구성(temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).

**데이터 집합 데이터 저장소에 대한 새 위치를 추가하려면**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.
1. 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 구성하고 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Disk Files.cfg] 파일이 이 디렉터리 내에 있습니다.
1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 [!DNL Disk Files.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Disk Files.cfg].
1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. 에서 [!DNL Disk Files.cfg] 창 **[!UICONTROL component]** 콘텐츠를 보려면 클릭하십시오.

   ![단계 정보](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >디스크 손상 검색 매개 변수는 기본적으로 true 로 설정됩니다. Disk Cache Size(MB) 매개 변수는 [!DNL Insight Server] 은 디스크 액세스 속도를 높이는 데 사용되며 기본적으로 128로 설정되어 있습니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. 에서 디스크 파일을 변경하려면 [!DNL Insight Server] 머신, 마우스 오른쪽 단추 클릭 **[!UICONTROL Disk Files]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > **[!UICONTROL Disk File]**.

   디스크 파일을 삭제하려면 디스크 파일 번호를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Remove]**.

1. 새 디스크 파일의 경우 사용할 파일의 디렉토리와 이름을 입력합니다 [!DNL Insight Server] 재처리 및 작업 중에

   ![단계 정보](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >디스크 손상 검색 매개 변수는 기본적으로 true 로 설정됩니다. Disk Cache Size(MB) 매개 변수는 [!DNL Insight Server] 은 디스크 액세스 속도를 높이는 데 사용되며 기본적으로 128로 설정되어 있습니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 선택 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
