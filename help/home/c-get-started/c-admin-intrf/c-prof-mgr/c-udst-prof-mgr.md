---
description: 구현에 포함된 폴더 및 파일 이름은 프로필 관리자 왼쪽에 표시됩니다.
title: 프로필 관리자
uuid: c3a19a56-c96b-4661-b656-b845feba4b6f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---


# 프로필 관리자{#profile-manager}

{{eol}}

구현에 포함된 폴더 및 파일 이름은 프로필 관리자 왼쪽에 표시됩니다.

애플리케이션을 구성하는 프로필은 [!DNL Profile Manager]. 이러한 프로필에는 상속된 여러 프로필과 하나의 작업 프로필이 포함됩니다.

>[!NOTE]
>
>작업 프로필(데이터 세트 프로필 또는 역할별 프로필)은 Data Workbench을 열 때 로드하는 프로필입니다.

확인 표시(및 해당 색상)는 Data Workbench 서버 및 각 파일이 있는 Data Workbench 컴퓨터의 프로필 폴더, 파일의 여러 복사본이 있는지 여부, 여러 복사본이 동일한 수정 날짜 및 시간을 가지는지 여부를 나타냅니다. 이러한 파일은 Data Workbench 서버와 Data Workbench 컴퓨터 간에 프로필 다운로드 중에 동기화됩니다.

다음은 샘플입니다 [!DNL Profile Manager] HBX 구현의 경우:

![](assets/client-prof.png)

에서 [!DNL Profile Manager] 메뉴를 선택하면 다른 관리자(예: [!DNL Dimensions Manager] 또는 [!DNL Reports Manager]). [!DNL Profile Manager]. 새 프로필 관리자를 만들 수도 있습니다. 자세한 내용은 [새 프로필 관리자 만들기](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-prof-files-mgrs/c-new-prof-mgrs.md#concept-0021e006523e4d538aaa16322731d9d3).

특정 열의 파일 이름 옆에 있는 확인 표시는 해당 이름의 파일이 해당 열(프로필)에 있는 폴더에 있음을 나타냅니다. 오른쪽의 오른쪽으로 이동할 때 [!DNL Profile Manager]파일이 왼쪽에 있는 프로필보다 우선합니다. 즉, 상속된 각 프로필은 [!DNL Profile Manager]. 예를 들어, 파일의 이름이 동일하고 파일의 위치가 [!DNL Base] 프로필(열) 및 [!DNL User] 프로필(열), 파일의 [!DNL User] 프로필은 의 파일 대신 사용됩니다 [!DNL Base] 프로필 참조.

## 프로필 검색 {#section-91f873f1d7ed4fd6a5f3c3ac08cfa623}

5.5 Data Workbench을 사용할 때에서 필수 프로필을 찾기 위한 검색 필드가 추가되었습니다. [!DNL Profile Manager].

![](assets/client-prof2.png)

다음 유형의 열은 [!DNL Profile Manager]:

* 다음 *상속된 프로필 이름* 열에는 각 프로필 폴더에 있는 파일의 확인 표시가 포함됩니다. 상속된 프로필에는 Adobe이 제공한 내부 프로필과 만들고 유지 관리하는 회사별 또는 역할별 프로필이 포함됩니다. 위의 예에서는 내부 프로필에 기본, 트래픽, 값, 마케팅 등이 포함됩니다. 내부 [!DNL Base] Adobe 응용 프로그램을 실행하는 데 필요한 기본 구성 요소와 구성 정보가 포함된 프로필은 모든 구현과 함께 제공됩니다. 다른 내부 프로필에는 웹 트래픽 또는 마케팅과 같은 특정 유형의 정보와 관련된 요소(작업 공간, 지표, 파생 차원 등)가 포함되어 있습니다. Adobe은 분석 중인 데이터 유형과 업계에 적합한 프로필만 제공합니다.

   >[!NOTE]
   >
   >기본적으로 내부 프로필(Adobe에서 제공한 프로필)은 변경할 수 없습니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다. 새 응용 프로그램을 작성하고 내부 프로파일을 변경해야 하는 경우, [!DNL Insight.cfg] 파일. 자세한 내용은 [인사이트 구성 매개 변수](../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b) 추가 정보. 이 작업을 수행하기 전에 Adobe 컨설팅 서비스에 문의하십시오.

* 다음 *작업 프로필 이름* 항상 다음으로 마지막 열인 열에는 현재 작업 프로필의 폴더에 있는 파일에 대한 확인 표시가 포함됩니다. 위의 예에서 작업 프로필은 데이터 세트입니다. 작업 프로필은 데이터 집합 프로필 또는 역할별 프로필입니다. 이 폴더의 파일이 상속된 프로필 폴더에서 이름이 같은 파일보다 우선합니다.
* 다음 [!DNL User] 항상 마지막 열인 열에는 User\*profile name* 폴더에 로컬 파일로 있는 파일과 폴더에 대한 확인 표시가 포함됩니다. 사용자 폴더의 디렉토리 구조는 작업 프로필의 디렉토리 구조와 유사하며 각 User\*profile name* 폴더에는 특정 프로파일에 대한 작업 공간, 지표, 차원 및 구성 파일의 로컬 복사본이 포함됩니다. 이러한 로컬 복사본은 상속되었거나 작업 프로필 폴더에서 이름이 같은 파일보다 우선합니다. 의 파일 [!DNL User] 열이 생성되어 User\*profile name* 폴더에만 저장되거나 내부 또는 작업 프로필과 User\*profile name* 폴더에 있습니다. 각 폴더의 파일은 동일하거나 동일하지 않을 수 있으며 동일한 수정 날짜 및 시간을 가질 수도 있고 가질 수도 있습니다.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * 데이터 세트를 로컬에서만 변경하지 않도록 Data Workbench 서버는 데이터 세트의 로컬 사본을 무시합니다 [!DNL profile.cfg] 파일 및 User\*profile name* 폴더의 데이터 집합 또는 내보내기 폴더에 있는 모든 파일. 무시된 파일은 [!DNL User] 컨텍스트 메뉴의 열과 &quot;사용자 디렉토리에서 무시됨&quot; 경고 이러한 파일의 로컬 복사본에서 변경한 내용을 구현하려면 작업 프로필에 변경 내용을 저장하여 Data Workbench 서버와 동기화해야 합니다. 작업 프로필에 파일을 저장하는 단계는 [작업 프로필에 파일 게시](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).
   >    
   >    * 열의 확인 표시 대신 하이픈(-)은 빈(0바이트) 파일을 식별합니다. Data Workbench은 0바이트 파일을 존재하지 않는 것으로 간주하여 프로필에 포함된 파일을 왼쪽으로 숨길 수 있습니다. 자세한 내용은 [빈(0바이트) 파일을 사용하여 파일 숨기기](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491).


## 파일 버전 확인 {#section-225d732246b94cbe87acdfa9c881d6af}

이전 섹션에서 설명한 대로 [!DNL Profile Manager] 파일이 있는 위치와 여러 번 파일의 여러 복사본을 수정했는지 여부를 쉽게 식별할 수 있도록 색상으로 구분됩니다.

파일 또는 축소된 디렉토리가 왼쪽에 있는 파일 또는 디렉토리와 정확히 동일한 경우 해당 열(프로파일)의 파일 또는 디렉토리와 동일한 색상 확인 표시가 나타납니다. 파일 또는 디렉토리와 왼쪽이나 다른 경우 또는 파일 또는 디렉토리가 [!DNL User] 열, 확인 표시는 흰색입니다.

![](assets/vis_ProfMgr_LocalFiles.png)

다음 [!DNL Profile Manager] 위의 예에 표시된 것은 다음을 나타냅니다.

* 에 대한 흰색 확인 표시 [!DNL A New Metric.metric] 파일에만 나타납니다. [!DNL User] 열은 해당 파일의 로컬 복사본만 가지고 있음을 나타냅니다. 다른 Data Workbench 사용자가 액세스할 수 있도록 Data Workbench 서버에 게시되지 않았거나 업로드되지 않았습니다.

* 에 대한 표시 확인 [!DNL Average Score.metric] 파일 이름이 동영상 및 [!DNL User] 열. 체크 표시는 [!DNL User] 열은 [동영상] 열의 확인 표시와 동일한 색상으로, 파일의 로컬 사본이 [동영상] 폴더의 파일과 같은 날짜 및 시간을 갖는다는 것을 나타냅니다.

* 에 대한 표시 확인 [!DNL Average Score Error.metric] 파일 이름이 동영상 및 [!DNL User] 열. 체크 표시는 [!DNL User] 열은 흰색이며, 파일의 로컬 복사본에 동영상 폴더의 파일과 다른 수정 날짜 또는 시간이 있음을 나타냅니다.

