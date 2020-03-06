---
description: 데이터 집합 모니터링과 데이터 집합 데이터 저장소의 새 위치 추가에 대한 정보입니다.
solution: Insight
title: 데이터 집합 데이터 공간 모니터링
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 집합 데이터 공간 모니터링{#monitoring-dataset-data-space}

데이터 집합 모니터링과 데이터 집합 데이터 저장소의 새 위치 추가에 대한 정보입니다.

**권장 빈도:** 5-10분마다

기본적으로 데이터 [!DNL Insight Server] 처리 장치의 프로그램 파일과 같은 드라이브에 있는 [!DNL temp.db] 파일에 데이터 [!DNL Insight Server] 세트를 씁니다. 시스템당 데이터 집합 데이터의 양은 다음 중 먼저 발생하는 것으로 [!DNL Insight Server] 제한됩니다.

* 해당 데이터 세트에 대한 데이터 입력 레코드 5억 개(5억 개)
* 500GB의 데이터 세트 데이터 저장
* 하나의 루트 수준 차원당 1MB의 데이터 세트 데이터 저장(예: 방문자당 평균 레코드당 5,000개 레코드)

데이터 세트를 다른 드라이브에서 [!DNL Insight Server] 유지하거나 수집할 데이터의 양이 여러 드라이브를 사용해야 하는 경우 디스크 파일 구성 파일( [!DNL Disk Files.cfg])을 업데이트하여 파일을 쓸 [!DNL Insight Server] [!DNL temp.db] 위치를 지정해야 합니다. 이 [!DNL Disk Files.cfg] [!DNL Insight Server] 파일은 디스크 파일(문자열 벡터)을 나열하고 재처리 및 작업 중에 사용되는 데이터 집합 데이터의 위치를 지정합니다. 일반적으로 물리적 드라이브당 파일이 하나씩 있습니다.

>[!NOTE]
>
>설치 중에 [!DNL Disk Files.cfg] 파일 내용이 수정되었을 수 [!DNL Insight Server]있습니다. 자세한 내용은 데이터 세트 [위치 구성(temp.db)을](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e)참조하십시오.

**데이터 집합 데이터 저장소에 대한 새 위치를 추가하려면**

1. > [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 구성할 아이콘 을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Disk Files.cfg] 파일은 이 디렉토리 내에 있습니다.
1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Disk Files.cfg] **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Disk Files.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Insight]**&#x200B;을 클릭합니다.
1. 창에서 [!DNL Disk Files.cfg] 을 클릭하여 내용을 **[!UICONTROL component]** 봅니다.

   ![단계 정보](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >디스크 손상 감지 매개 변수는 기본적으로 true로 설정됩니다. Disk Cache Size (MB) 매개 변수는 디스크 액세스 속도를 높이는 데 [!DNL Insight Server] 사용하는 메모리 양을 제어하고 기본적으로 128로 설정합니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. 시스템의 디스크 파일을 변경하려면 [!DNL Insight Server] 마우스 오른쪽 버튼을 클릭한 **[!UICONTROL Disk Files]** 다음 **[!UICONTROL Add new]** > **[!UICONTROL Disk File]**&#x200B;를 클릭합니다.

   디스크 파일을 삭제하려면 디스크 파일 번호를 마우스 오른쪽 버튼으로 클릭한 다음 을 **[!UICONTROL Remove]**&#x200B;클릭합니다.

1. 새 디스크 파일의 경우 재처리 및 작업 [!DNL Insight Server] 중에 사용할 파일의 디렉토리 및 이름을 입력합니다.

   ![단계 정보](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >디스크 손상 감지 매개 변수는 기본적으로 true로 설정됩니다. Disk Cache Size (MB) 매개 변수는 디스크 액세스 속도를 높이는 데 [!DNL Insight Server] 사용하는 메모리 양을 제어하고 기본적으로 128로 설정합니다. 이러한 매개 변수 중 하나를 변경하기 전에 Adobe에 문의하십시오.

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *를 선택합니다&#x200B;**[!UICONTROL server name]***.

