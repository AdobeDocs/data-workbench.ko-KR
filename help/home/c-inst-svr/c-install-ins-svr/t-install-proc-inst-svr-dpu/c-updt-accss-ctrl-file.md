---
description: Access Control.cfg 파일은 Insight Server의 특정 기능에 대한 액세스를 관리합니다.
solution: Insight
title: 액세스 제어 파일 업데이트
uuid: f73651e5-6a8b-45fc-8f36-6751304dc53c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 액세스 제어 파일 업데이트{#updating-the-access-control-file}

Access Control.cfg 파일은 Insight Server의 특정 기능에 대한 액세스를 관리합니다.

AccessGroups라는 엔터티를 정의합니다. AccessGroup은 서버의 특정 기능을 사용할 수 있는 권한이 있는 사용자 그룹을 식별합니다.

Adobe [!DNL Insight Server] 가 조직에 발급한 라이선스 중 하나를 포함하도록 Administrators AccessGroup을 [!DNL Insight]업데이트해야 합니다 [!DNL Insight] . 이 AccessGroup은 을 통해 관리 기능을 수행할 수 있는 사용자를 [!DNL Insight]식별합니다.

다음 절차에서는 관리자 액세스 그룹에 라이선스를 추가하는 방법에 대해 설명합니다. 이 작업을 완료하려면 조직에 대한 관리 권한이 있는 [!DNL Insight] 라이선스를 결정해야 합니다. (초기 설정 및 구성의 경우 단일 라이센스에 관리 권한을 부여하는 것이면 충분합니다. 나중에 추가 라이선스에 대한 관리 권한을 부여할 수 있습니다.) 또한 이 라이선스에 할당된 &quot;일반 이름&quot;을 알고 있어야 합니다. 이 값을 받으려면 https://aap.adobe.com에서 계정에 대한 라이센스 인증서를 검사할 수 [있습니다](https://aap.adobe.com).

이 절차의 목적은 처음에 설정 및 구성하는 데 사용할 수 [!DNL Insight] 있는 라이센스 사본을 식별하는 [!DNL Insight Server]것입니다. 이 라이센스를 식별하면 라이센스가 부여된 복사본을 사용하여 모든 후속 서버 구성(추가 AccessGroup 구성 포함)을 수행할 수 [!DNL Insight]있습니다. AccessGroups를 사용하여 서버에 대한 액세스 제어에 대한 자세한 내용은 액세스 제어 [구성을 참조하십시오](../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d).

**액세스 제어 파일을 업데이트하려면**

1. 설치한 디렉토리의 [!DNL Access Control] 폴더로 [!DNL Insight Server]이동합니다.

   예: [!DNL C:\Adobe\Server\Access Control]

1. 메모장과 같은 텍스트 편집기에서 파일을 [!DNL Access Control.cfg] 엽니다.
1. Administrators AccessGroup에서 CN 항목을 찾고 이 항목의 기존 값을 처음에 설정 및 관리하는 데 사용할 [!DNL Insight] 항목을 식별하는 일반 이름으로 바꿉니다 [!DNL Insight Server]. 다음 파일 조각은 [!DNL Access Control.cfg] 파일에서 공통 이름을 삽입하는 위치를 보여줍니다.

   ```
   Access Control Groups = vector: 5 items 
     0 = AccessGroup: 
       Members = vector: 2 items 
         0 = string: IP:127.0.0.1 
         1 = string: CN: CommonName 
       Name = string: Administrators 
       Read-Only Access = vector: 0 items 
       Read-Write Access = vector: 1 items 
         0 = string: / 
     1 = AccessGroup: 
     . . . 
   ```

   자격 증명 기반 인증을 사용하는 경우 구성에 몇 가지 추가 항목을 사용할 수 있습니다. 이러한 항목은 다음과 같습니다.

   * O(조직 ID):이 항목은 조직의 ID를 나타냅니다. (예: `1 = string: O:46F582D4582596B40A45491@ExampleOrg`) 이 ID는 관리 콘솔에서 찾을 수 있습니다.
   * PLC - 이 항목을 사용하면 특정 제품 구성에 대해 제공된 사용자에게 액세스할 수 있습니다. 포맷으로 사용할 수 `Organization_Id-PLC`있습니다. (예: `1 = string: PLC:46F582D4582596B40A45491@ExampleOrg-DataworkbenchAdminUsers`) PLC를 사용하여 Data Workbench에 프로비저닝된 사용자는 서버에서 액세스할 수 `DataworkbenchAdminUsers` 있습니다.
   * 이메일 - 이 항목을 사용하면 개별 사용자에게 액세스할 수 있습니다. 이 값은 제공된 사용자의 이메일 주소여야 합니다. (예: `1 = string: Email:kim@exampleorg.com`)
   >[!NOTE]
   >
   >
   >    
   >    
   >    * 항목은 대소문자를 구분합니다. O, PLC 및 Email에 대해 지정된 값이 Admin Console에 표시된 값과 정확히 동일한지 확인해야 합니다.
   >    * 인증서에 표시되는 것과 동일한 일반 이름을 입력합니다.
   >    * Tab 키를 사용하여 [!DNL Access Control.cfg] 파일(또는 Adobe 구성 요소의 다른 구성 파일)에 공백을 생성하지 마십시오. 공백만 사용하여 공백을 만듭니다. 탭 문자를 사용하면 시스템이 파일을 제대로 읽지 못합니다.


1. 파일을 저장하고 닫습니다.
