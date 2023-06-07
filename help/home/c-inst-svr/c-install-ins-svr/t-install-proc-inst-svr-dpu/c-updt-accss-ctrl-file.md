---
description: Access Control.cfg 파일은 Insight Server의 특정 기능에 대한 액세스를 관리합니다.
title: 액세스 제어 파일 업데이트
uuid: f73651e5-6a8b-45fc-8f36-6751304dc53c
exl-id: 551758c1-f24b-49e6-ab6e-09979511e4f4
source-git-commit: 5ce5b8f8b35d2d4f319076f54347e300e5f133df
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 3%

---

# 액세스 제어 파일 업데이트{#updating-the-access-control-file}

{{eol}}

Access Control.cfg 파일은 Insight Server의 특정 기능에 대한 액세스를 관리합니다.

AccessGroups라는 엔터티를 정의합니다. AccessGroup은 서버의 특정 기능을 사용할 수 있는 권한이 있는 사용자 그룹을 식별합니다.

에 연결하기 전에 [!DNL Insight Server] 포함 [!DNL Insight], 관리자 액세스 그룹 을 업데이트하여 다음 중 하나를 포함해야 합니다. [!DNL Insight] 해당 Adobe이 조직에 발급한 라이선스. 이 AccessGroup은 다음을 통해 관리 기능을 수행하도록 허용된 사용자를 식별합니다. [!DNL Insight].

다음 절차에서는 Administrators AccessGroup에 라이선스를 추가하는 방법을 설명합니다. 이 작업을 완료하려면 다음을 결정해야 합니다. [!DNL Insight] 라이선스에는 조직에 대한 관리 권한이 있습니다. 초기 설정 및 구성의 경우 단일 라이센스에 관리 권한을 부여하면 됩니다. 나중에 추가 라이센스에 대한 관리 권한을 부여할 수 있습니다.) 또한 이 라이센스에 할당된 &quot;일반 이름&quot;도 알고 있어야 합니다.

이 절차의 목적은 라이선스가 부여된 사본을 식별하는 것입니다. [!DNL Insight] 를 사용하여 처음에 설정 및 구성할 수 있습니다. [!DNL Insight Server]. 이 라이센스를 식별한 후에는 라이센스가 부여된 의 복사본을 사용하여 모든 후속 서버 구성(추가 AccessGroup 구성 포함)을 수행할 수 있습니다. [!DNL Insight]. AccessGroups를 사용하여 서버에 대한 액세스를 제어하는 방법에 대한 자세한 내용은 [액세스 제어 구성](../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d).

**액세스 제어 파일을 업데이트하려면**

1. 다음 위치로 이동 [!DNL Access Control] 를 설치한 디렉토리의 폴더 [!DNL Insight Server].

   예: [!DNL C:\Adobe\Server\Access Control]

1. 를 엽니다. [!DNL Access Control.cfg] 메모장과 같은 텍스트 편집기의 파일입니다.
1. Administrators AccessGroup에서 CN 항목을 찾고 이 항목의 기존 값을 [!DNL Insight] 를 사용하여 처음에 설정 및 관리할 수 있습니다. [!DNL Insight Server]. 다음 파일 조각은에서 일반 이름을 삽입하는 위치를 보여 줍니다. [!DNL Access Control.cfg] 파일.

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

   자격 증명 기반 인증을 사용하는 경우 구성에 몇 가지 추가 항목을 사용할 수 있습니다. 이 항목은 다음과 같습니다.

   * O (조직 ID): 이 항목은 조직의 ID를 나타냅니다. (예: `1 = string: O:46F582D4582596B40A45491@ExampleOrg`) 이 ID는 Admin Console에서 찾을 수 있습니다.
   * PLC - 이 항목은 특정 제품 구성에 대해 프로비저닝된 사용자에 대한 액세스를 허용합니다. 형식으로 사용할 수 있습니다 `Organization_Id-PLC`. (예: `1 = string: PLC:46F582D4582596B40A45491@ExampleOrg-DataworkbenchAdminUsers`) PLC를 사용하여 Data Workbench을 제공한 사용자 `DataworkbenchAdminUsers` 은(는) 해당 서버에 대한 액세스 권한을 받습니다.
   * 이메일 - 이 항목은 개별 사용자에 대한 액세스를 허용합니다. 해당 값은 프로비저닝된 사용자의 이메일 주소여야 합니다. (예: `1 = string: Email:kim@exampleorg.com`)

   >[!NOTE]
   >
   >
   >    
   >    
   >    * 항목은 대/소문자를 구분합니다. O, PLC 및 이메일에 대해 지정된 값이 Admin Console에 표시된 값과 정확히 동일한지 확인해야 합니다.
   >    * 인증서에 표시되는 일반 이름을 정확히 입력합니다.
   >    * Tab 키를 사용하여 [!DNL Access Control.cfg] 파일(또는 Adobe 구성 요소에 대한 다른 구성 파일)을 참조하십시오. 공백만 사용하여 공백을 만드십시오. 탭 문자로 인해 시스템이 파일을 올바르게 읽을 수 없습니다.


1. 파일을 저장하고 닫습니다.
