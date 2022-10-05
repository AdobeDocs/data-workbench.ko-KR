---
description: 로그 처리 데이터 집합에 정의된 웹 특정 설정에 대한 정보에는 사이트의 Adobe 프로필과 함께 제공되는 파일이 포함됩니다.
title: 로그 처리를 위한 웹 특정 설정
uuid: dea861a6-3f78-4cb9-8108-ecf397b37667
exl-id: abb6e6a7-011f-40d6-b778-16da2332af72
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 1%

---

# 로그 처리를 위한 웹 특정 설정{#web-specific-settings-for-log-processing}

{{eol}}

로그 처리 데이터 집합에 정의된 웹 특정 설정에 대한 정보에는 사이트의 Adobe 프로필과 함께 제공되는 파일이 포함됩니다.

이러한 설정에 의해 정의된 필터링은 로그 항목이 디코더와 변형을 적용한 후 [!DNL Log Entry Condition].

* [HTTP 상태 필터링](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-ac66acdcb6aa467d81c3721199e540fd)
* [로봇 필터링](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-7f43681dfbc64b969619cb88f97d5ad5)

## HTTP 상태 필터링 {#section-ac66acdcb6aa467d81c3721199e540fd}

구현을 구성할 수 있습니다 [!DNL Site] 데이터 세트에서 sc 상태 코드가 400 이상인 로그 항목을 제거하려면 다음을 수행하십시오. 성공적인 요청에는 400보다 적은 상태 코드가 있습니다. 기본 구현에는 다음이 포함됩니다 [!DNL Log Processing Dataset Include] HTTP 상태 필터링이 구성된 파일입니다.

**HTTP 상태 필터링에 대한 구성 설정을 편집하려면**

1. 를 엽니다. [!DNL Profile Manager] 데이터 세트 프로필 내에서 를 열고 [!DNL Dataset\Log Processing\Traffic\HTTP Status Filter.cfg] 파일.

   >[!NOTE]
   >
   >구현을 사용자 정의한 경우 [!DNL Site]로 지정하는 경우 이러한 구성 설정이 있는 파일이 설명된 위치와 다를 수 있습니다.

1. 원하는 대로 파일의 매개 변수 값을 검토하거나 편집합니다. 다음 예를 안내서로 사용합니다.

   ![](assets/cfg_WebParameters_HTTPStatusFilter.png)

   에 대한 정보 [!DNL Range] 조건: [조건](../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md).

1. 를 저장합니다 [!DNL HTTP Status Filter.cfg] 마우스 오른쪽 단추를 클릭하여 파일 만들기 **[!UICONTROL (modified)]** 창 상단에서 **[!UICONTROL Save]**.

1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;여기서 프로필 이름은 데이터 집합 프로필 또는 데이터 집합에 포함된 파일이 속한 상속된 프로필의 이름입니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.

## 로봇 필터링 {#section-7f43681dfbc64b969619cb88f97d5ad5}

구현을 구성할 수 있습니다 [!DNL Site] 조회 파일을 사용하여 알려진 로봇에 의해 생성된 로그 항목, 테스트 스크립트 및 데이터 세트에서 내부 사용자에 대한 IP 주소를 제거합니다. 기본 구현에는 다음이 포함됩니다 [!DNL Log Processing Dataset Include] 로봇 필터링이 구성된 파일입니다.

**로봇 필터링에 대한 구성 설정을 편집하려면**

1. 를 엽니다. [!DNL Profile Manager] 데이터 세트 프로필 내에서 를 열고 [!DNL Dataset\Log Processing\Traffic\Robot Filter.cfg] 파일.

   >[!NOTE]
   >
   >구현을 사용자 정의한 경우 [!DNL Site]로 지정하는 경우 이러한 구성 설정이 있는 파일이 설명된 위치와 다를 수 있습니다.

1. 다음 예와 정보를 안내서로 사용하여 파일의 매개 변수를 검토하거나 편집합니다.

   ![](assets/cfg_WebParameters_RobotFilter.png)

   파일에는 다음이 포함되어 있습니다 [!DNL NotRobotCondition] 다음 세 매개 변수로 정의됩니다.

   * **대/소문자 구분 로봇 필터링:** True 또는 False입니다. true일 경우 로봇 필터링에서 대소문자(위/아래)는 고려되지 않습니다.
   * **로봇 조회 파일, 베이스라인:** 알려진 로봇이며 데이터 집합에서 필터링될 브라우저 사용자 에이전트 목록이 포함된 텍스트 파일의 경로 및 파일 이름입니다. Adobe은 베이스라인 로봇 조회 파일을 제공합니다. 경로를 지정하지 않으면 Data Workbench 서버가 Data Workbench 서버 설치 디렉토리 내의 조회 디렉토리에서 이 파일을 찾습니다.
   * **로봇 조회 파일, 확장:** 구현과 관련된 로봇을 정의하는 브라우저 사용자 에이전트 또는 IP 주소 목록을 포함하는 선택적 텍스트 파일의 경로 및 파일 이름입니다. 이 목록에는 데이터 집합에서 필터링해야 하는 내부 사용자에 대한 내부 모니터링 로봇, 테스트 스크립트 및 IP 주소가 포함될 수 있습니다. 경로를 지정하지 않으면 Data Workbench 서버가 Data Workbench 서버 설치 디렉토리 내의 조회 디렉토리에서 이 파일을 찾습니다.

   로그 항목의 브라우저 사용자 에이전트가 조회 파일에 나열되지 않으면 로그 항목은 실제 방문자가 생성한 것으로 간주되며 데이터 집합에서 필터링되지 않습니다.

   >[!NOTE]
   >
   >로봇 조회 파일에서 일치하면 하위 문자열을 사용하여 c-ip 및 cs(user-agent) 로그 필드와 비교합니다. 검색 문자열이 &quot;$&quot;로 시작하는 경우 테스트 중인 문자열 앞면과 일치해야 하며 &quot;$&quot;로 끝나는 경우 검색 문자열은 테스트 중인 문자열 끝과 일치해야 합니다. 검색 문자열이 &quot;$&quot;로 시작하고 끝나는 경우 문자열을 정확히 일치해야 로그 항목을 필터링할 수 있습니다. 예를 들어 클래스 C 블록의 모든 IP 주소를 테스트하려면 $231.78.123. 등의 문자열을 사용하여 문자열 앞부분에서 일치 항목을 적용합니다. 이 경우 주소가 231.78.123.0 ~ 231.78.123.255.

1. 마우스 오른쪽 단추를 클릭하여 파일을 저장합니다 **[!UICONTROL (modified)]** 창 상단에서 **[!UICONTROL Save]**.

1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;여기서 프로필 이름은 데이터 집합 프로필 또는 데이터 집합에 포함된 파일이 속한 상속된 프로필의 이름입니다.

   이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.

   >[!NOTE]
   >
   >데이터 집합을 구성하는 데 사용되는 기본 로그 항목이 변경되지 않는 것이 중요한 경우(데이터 집합 및 해당 차원을 구성하고 업데이트하는 데 사용되는 변환이 변경되더라도) 로봇 조회 파일, 기준선 및 로봇 조회 파일, 확장자를 버전 제어해야 합니다. 이러한 파일에 버전 번호를 지정하면 기본 로봇 조회 파일에 대한 업데이트가 이러한 파일의 항목을 추가하거나 삭제하여 이전에 구성한 보고 데이터 세트를 실수로 변경하지 않습니다.
