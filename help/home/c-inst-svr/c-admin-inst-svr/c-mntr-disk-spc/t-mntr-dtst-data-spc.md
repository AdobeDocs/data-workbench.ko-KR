---
description: 데이터 집합 데이터 저장소에 대한 데이터 집합 모니터링 및 새 위치 추가에 대한 정보입니다.
solution: Analytics
title: 데이터 집합 데이터 공간 모니터링
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---


# 데이터 집합 데이터 공간 모니터링{#monitoring-dataset-data-space}

데이터 집합 데이터 저장소에 대한 데이터 집합 모니터링 및 새 위치 추가에 대한 정보입니다.

**권장 빈도:** 5-10분마다

기본적으로 데이터 [!DNL Insight Server] 처리 장치의 프로그램 파일과 같은 드라이브에 있는 [!DNL temp.db] 파일에 데이터 세트 [!DNL Insight Server] 를 씁니다. 시스템당 데이터 집합 데이터 [!DNL Insight Server] 의 양은 다음 중 먼저 발생하는 것으로 제한됩니다.

* 해당 데이터 세트에 5억 개의 데이터 입력 레코드
* 500GB의 데이터 세트 데이터 저장
* 하나의 루트 수준 차원당 1MB의 데이터 세트 데이터 저장(예: 방문자당 평균 200바이트의 5,000개 레코드)

데이터 세트 [!DNL Insight Server] 를 다른 드라이브에 유지하려는 경우 또는 수집할 데이터의 양이 여러 드라이브를 사용해야 하는 경우 디스크 파일 구성 파일( [!DNL Disk Files.cfg])을 업데이트하여 파일을 쓸 위치 [!DNL Insight Server] [!DNL temp.db] 를 지정해야 합니다. 이 [!DNL Disk Files.cfg] 파일은 디스크 파일(문자열 벡터)을 나열하고 재처리 및 작업 중에 사용되는 데이터 세트 데이터 [!DNL Insight Server] 의 위치를 지정합니다. 보통 물리적 드라이브당 파일이 한 개 있습니다.

>[!NOTE]
>
>설치 중에 파일 [!DNL Disk Files.cfg] 내용이 수정되었을 수 있습니다 [!DNL Insight Server]. 자세한 내용은 데이터 세트 [의 위치 구성(temp.db)을 참조하십시오](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).

**데이터 집합 데이터 저장소에 대한 새 위치를 추가하려면**

1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.
1. 구성할 아이콘 [!DNL Insight Server] 을 마우스 오른쪽 단추로 클릭하고 클릭합니다 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Components]** 를 봅니다. 이 디렉터리 내에 [!DNL Disk Files.cfg] 파일이 있습니다.
1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 [!DNL Disk Files.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 열에 확인 표시가 [!DNL Temp] 나타납니다 [!DNL Disk Files.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** 를 **[!UICONTROL in Insight]**&#x200B;클릭합니다.
1. 창에서 [!DNL Disk Files.cfg] 을 클릭하여 내용 **[!UICONTROL component]** 을 봅니다.

   ![단계 정보](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >디스크 손상 감지 매개 변수는 기본적으로 true로 설정됩니다. 디스크 캐시 크기(MB) 매개 변수는 디스크 액세스 속도를 높이는 데 [!DNL Insight Server] 사용하는 메모리의 양을 제어하며 기본적으로 128로 설정됩니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. 시스템의 디스크 파일을 변경하려면 [!DNL Insight Server] 마우스 오른쪽 단추를 클릭하고 > **[!UICONTROL Disk Files]** 를 **[!UICONTROL Add new]** 클릭합니다 **[!UICONTROL Disk File]**.

   디스크 파일을 삭제하려면 디스크 파일 번호를 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Remove]**.

1. 새 디스크 파일의 경우 재처리 및 작업 중에 사용할 파일의 디렉토리 및 이름을 [!DNL Insight Server] 입력합니다.

   ![단계 정보](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >디스크 손상 감지 매개 변수는 기본적으로 true로 설정됩니다. 디스크 캐시 크기(MB) 매개 변수는 디스크 액세스 속도를 높이는 데 [!DNL Insight Server] 사용하는 메모리의 양을 제어하며 기본적으로 128로 설정됩니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 위쪽 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 열 [!DNL Server Files Manager]에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 선택합니다&#x200B;**[!UICONTROL server name]***.

