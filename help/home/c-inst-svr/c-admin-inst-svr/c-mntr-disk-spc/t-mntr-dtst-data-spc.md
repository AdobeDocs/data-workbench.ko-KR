---
description: 데이터 집합 데이터 저장을 위한 데이터 집합 모니터링 및 새 위치 추가에 대한 정보입니다.
title: 데이터 세트 데이터 공간 모니터링
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
exl-id: eb34d5fe-73c6-461f-8bb0-85833d8f824f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---

# 데이터 세트 데이터 공간 모니터링{#monitoring-dataset-data-space}

데이터 집합 데이터 저장을 위한 데이터 집합 모니터링 및 새 위치 추가에 대한 정보입니다.

**권장 빈도:** 5-10분마다

기본적으로 [!DNL Insight Server]은 데이터 처리 단위의 [!DNL Insight Server] 프로그램 파일과 동일한 드라이브의 [!DNL temp.db] 파일에 데이터 세트를 씁니다. [!DNL Insight Server] 컴퓨터당 데이터 집합 데이터의 양은 다음 중 먼저 발생하는 것으로 제한됩니다.

* 해당 데이터 세트에 대한 데이터 입력 기록 5억 (5억 개)
* 500GB의 데이터 세트 데이터 저장
* 하나의 루트 수준 차원당 1MB의 데이터 세트 데이터 저장(예: 방문자당 평균 레코드당 5,000개의 레코드)

[!DNL Insight Server]이(가) 다른 드라이브에 있는 데이터 세트를 유지하려는 경우 또는 수집할 데이터의 양이 여러 드라이브를 사용해야 하는 경우 [!DNL Insight Server]에서 [!DNL temp.db] 파일을 쓸 위치를 지정하려면 디스크 파일 구성 파일( [!DNL Disk Files.cfg])을 업데이트해야 합니다. [!DNL Disk Files.cfg] 파일은 디스크 파일(문자열 벡터)을 나열하고 재처리 및 작업 중 [!DNL Insight Server]에서 사용하는 데이터 집합 데이터의 위치를 지정합니다. 보통 물리적 드라이브당 파일이 한 개 있습니다.

>[!NOTE]
>
>[!DNL Insight Server] 설치 중에 [!DNL Disk Files.cfg] 파일의 내용이 수정되었을 수 있습니다. 자세한 내용은 [데이터 세트 위치 구성(temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e)을 참조하십시오.

**데이터 집합 데이터 저장소에 대한 새 위치를 추가하려면**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 구성할 [!DNL Insight Server] 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 을 클릭합니다.
1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 콘텐트를 봅니다. [!DNL Disk Files.cfg] 파일이 이 디렉터리 내에 있습니다.
1. [!DNL Disk Files.cfg]에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. [!DNL Disk Files.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.
1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다.
1. [!DNL Disk Files.cfg] 창에서 **[!UICONTROL component]**&#x200B;을 클릭하여 내용을 봅니다.

   ![단계 정보](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >디스크 손상 감지 매개 변수는 기본적으로 true로 설정됩니다. 디스크 캐시 크기(MB) 매개 변수는 [!DNL Insight Server]이(가) 디스크 액세스 속도를 높이는 데 사용하는 메모리 양을 제어하며 기본적으로 128로 설정됩니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. [!DNL Insight Server] 컴퓨터의 디스크 파일을 변경하려면 **[!UICONTROL Disk Files]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Disk File]**&#x200B;를 클릭합니다.

   디스크 파일을 삭제하려면 디스크 파일 번호를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Remove]** 을 클릭합니다.

1. 새 디스크 파일의 경우 재처리 및 작업 중에 [!DNL Insight Server]에서 사용할 파일의 디렉토리 및 이름을 입력합니다.

   ![단계 정보](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >디스크 손상 감지 매개 변수는 기본적으로 true로 설정됩니다. 디스크 캐시 크기(MB) 매개 변수는 [!DNL Insight Server]이(가) 디스크 액세스 속도를 높이는 데 사용하는 메모리 양을 제어하며 기본적으로 128로 설정됩니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 선택합니다.
