---
description: 관리자는 워크스테이션 사용자에게 사용자 지정 그룹에 대한 액세스 제어를 관리할 수 있는 능력을 부분적으로 제공할 수 있습니다.
title: 그룹 구성원 액세스에 대한 사용자 관리
uuid: c31128f9-1094-4337-9bf6-96401278df33
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# User Administration of Group Member Access{#user-administration-of-group-member-access}

관리자는 워크스테이션 사용자에게 사용자 지정 그룹에 대한 액세스 제어를 관리할 수 있는 능력을 부분적으로 제공할 수 있습니다.

**그룹 구성원 액세스에** 대한 자체 관리 권한은 관리자가 아닌 사람에게 사용자 지정 그룹의 구성원을 추가하거나 삭제할 수 있는 권한을 제공합니다. 관리자는 사용자 **목록** 파일을 만들고 새 그룹 구성원에 대한 Access Control.cfg [파일에서 그룹](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/admin-dwb-server/access-control/c-config-acs-ctrl.html) 액세스 권한을 설정합니다.

**서버 관리자 액세스**

파일을 **[!DNL User List]** 설정하고 파일과 동기화하면 서버 관리자 **[!DNL Communications.cfg]** 작업 **영역에서 수행됩니다** .

1. 워크플로우에서 관리 탭 > **데이터** 세트 및 **프로필 탭을** 클릭합니다.

1. 서버 관리자 **작업 영역을** 엽니다.
1. 다이어그램에서 마우스 오른쪽 단추를 클릭하고&#x200B;*서버 이름*>을 **선택합니다**.

   서버 파일은 열 파일, *임시*&#x200B;및 *`<server name>`*&#x200B;임시 테이블이 있는 테이블에서 *열립니다*.

1. **서버** 파일의 서버 열을 마우스 오른쪽 단추로 클릭하여 로컬으로 **[!DNL Access Control]** 만듭니다(이 기능 및 **[!DNL Components/Communications.cfg)]**&#x200B;에 대해).

   임시 열에 흰색 확인 표시가 **나타납니다** . 임시 폴더에서 편집할 수 있습니다. 그런 다음 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **서버에 저장을** 클릭합니다. 서버와 동기화하면 빨간색으로 바뀝니다.

## 사용자 List.cfg 파일 만들기 {#section-c25bcaf34f4546e6b8b65f5e7f69ac09}

관리자는 폴더에 **[!DNL User List.cfg]** 파일을 만들어야 합니다 **[!DNL Access Control]** .

1. 임시 열에서 마우스 오른쪽 버튼을 클릭** 액세스 제어** 행을 **클릭하고** 열기 **>** 폴더를 **선택합니다**. ![](assets/6_4_workstation_groups_3.png)

   임시 폴더의 액세스 제어 폴더가 **열리고** 단일 **[!DNL Access Control.cfg]** 파일이 나열됩니다.

1. 이 폴더에 다른 텍스트 파일을 추가하고 이름을 지정합니다( **[!DNL User List.cfg]** 옆에 **[!DNL Access Control.cfg]**).

1. Add the following parameters to the **[!DNL User List.cfg]** file.

사용자 목록 파일에는 AccessGroup 개체의 벡터가 **포함되어야** 하며 **각** AccessGroup **개체에는 Members라는 문자열**&#x200B;벡터가 있어야 합니다.

```
Access Control Groups = vector: 1 items 
  0 = AccessGroup:  
    Name = string: Group 1 
    Members = vector: 1 items 
      0 = string: CN:Joe User
```

그런 다음 **[!DNL User List.cfg]**파일의 워크스테이션 보기에서 사용자를 편집하고 추가할 수 있습니다.

![](assets/6_4_workstation_groups_4.png)

다음은 **[!DNL User List.cfg]** 파일에 추가할 기본 매개 변수입니다. 그런 다음 워크스테이션 보기에서 구성원을 추가할 수 있습니다.

```
Access Control Groups = vector: 1 items 
  0 = AccessGroup:  
    Name = string:  
    Members = vector: 0 items
```

>[!IMPORTANT]
>
>수동으로 편집하는 모든 **[!DNL .cfg]** 파일에서처럼 탭 대신 공백을 사용하고 공백과 구문에 주의를 기울여야 합니다. 이 파일의 오류로 인해 Adobe Insight *Server에서* 사용자 목록 파일을 무시합니다.

각 **액세스** 그룹의 이름 **필드는** [!DNL Access Control.cfg] 파일 내에서 참조됩니다.

>[!NOTE]
>
>CN과 같은 디렉토리 서비스 접두사가 있는 유효한 **멤버만** 또는 **OU:** 가 허용되고 와일드카드 문자(*)를 포함할 수 없습니다.

## Communications.cfg 파일 설정 {#section-9d6f05ba81c14f15be63e361533459e8}

관리자는 먼저 **[!DNL Components]> 파일을 열고 이름을 가진 새 키를 추가하여 이 기능을 활성화합니다[!DNL Communications.cfg]**.**[!DNL Access Control User List File]**이 키의 문자열 값은 이 새 파일이 위치할 경로입니다.

1. 서버 파일에서 구성 **요소를** 클릭하고 서버 열에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [로컬로 **만들기]를**&#x200B;클릭합니다.

   임시 열에 흰색 확인 표시가 **나타납니다** .

1. 임시 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **열기** > **워크스테이션에서** 을 **선택합니다**.

1. Communication. **cfg** 파일에서 구성 요소를 **마우스 오른쪽 단추로 클릭하고** 사용자 지정 키 **추가를선택합니다.** ![](assets/6_4_workstation_groups.png)

1. Access **Control 사용자** 목록 *파일로* 이름을 **입력하고** Type *을 String*&#x200B;으로설정합니다.

   >[!NOTE]
   새 목록 파일은 경로로 만들 수 없습니다. 이 문제를 해결하려면 파일을 저장하고 편집기(메모장)에서 파일을 열고 &quot;문자열&quot;을 &quot;경로&quot;로 변경해야 합니다.

   :

   ```
   component = CommServer:  
     Access Control File = Path: Access Control\\Access Control.cfg 
     Access Control User List File =  
    <string>: Access Control\\User List.cfg
   ```

   후:

   ```
   component = CommServer:  
     Access Control File = Path: Access Control\\Access Control.cfg 
     Access Control User List File =  
    <Path>: Access Control\\User List.cfg
   ```

1. 파일을 저장하고(필요한 경우) 서버에 저장합니다. **[!DNL Communications.cfg]** 이렇게 하면 **[!DNL Communications.cfg]** 파일이 파싱되지 않도록 오류가 발생하지 않도록 서버에서 구성 요소를 다시 시작합니다.
1. 시스템에 처리 서버가 포함된 경우 **[!DNL Components for Processing Servers.cfg]** 파일에서 구성 파일을 수정합니다.
1. 마우스 오른쪽 버튼을 클릭하여 **[!DNL Communications.cfg]** 서버에 저장합니다.

이제 데이터 워크벤치 관리자는 의도한 사용자가 사용자 목록 파일에 액세스할 수 있는지 확인하고 사용자가 그룹을 관리하도록 허용할 수 있습니다. 사용자는 사용자 목록 파일을 열고, 편집하고, 필요에 따라 CN 또는 OU 멤버를 추가 및 제거할 수 있습니다.

## Access Control.cfg 파일 동기화 {#section-ca6da453dfb4432bb40b86ef15ede872}

관리자는 사용자 목록 **[!DNL Access Control.cfg]** 파일에서 정의한 그룹에 대한 참조를 편집하고 삽입할 *수* 있습니다.

그룹에 대한 참조는 다른 멤버처럼 삽입해야 하지만 다음 구문을 사용합니다.

```
$(Group Name)
```

여기서 &quot;그룹 이름&quot;은 공백을 포함하여 사용자 목록 파일에 정의된 내용과 일치합니다. ![](assets/6_4_workstation_groups_2.png)

이 시점에서 데이터 워크벤치 관리자는 선택한 그룹 사용자가 사용자 목록 파일에 액세스할 수 있는지 확인할 수 있습니다. 그런 다음 선택한 사용자가 **[!DNL User List.cfg]** 파일을 열고 편집하고 필요에 따라 CN 또는 OU 멤버를 추가 및 제거할 수 있습니다.
