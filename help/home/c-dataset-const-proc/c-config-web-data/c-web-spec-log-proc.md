---
description: 로그 처리 데이터 세트에 정의된 웹 전용 설정에 대한 정보 사이트용 Adobe 프로파일과 함께 제공되는 파일을 포함합니다.
solution: Analytics
title: 로그 처리를 위한 웹 전용 설정
topic: Data workbench
uuid: dea861a6-3f78-4cb9-8108-ecf397b37667
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 로그 처리를 위한 웹 전용 설정{#web-specific-settings-for-log-processing}

로그 처리 데이터 세트에 정의된 웹 전용 설정에 대한 정보 사이트용 Adobe 프로파일과 함께 제공되는 파일을 포함합니다.

이러한 설정에 의해 정의된 필터링은 로그 항목이 디코더를 종료하고 변형을 적용한 후에 [!DNL Log Entry Condition]실행됩니다.

* [HTTP 상태 필터링](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-ac66acdcb6aa467d81c3721199e540fd)
* [로봇 필터링](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-log-proc.md#section-7f43681dfbc64b969619cb88f97d5ad5)

## HTTP 상태 필터링 {#section-ac66acdcb6aa467d81c3721199e540fd}

데이터 세트에서 sc 상태 코드가 400 이상인 로그 항목을 제거하도록 구현을 구성할 [!DNL Site] 수 있습니다. 성공한 요청에는 상태 코드가 400개 미만입니다. 기본 구현에는 HTTP 상태 필터링이 구성된 [!DNL Log Processing Dataset Include] 파일이 포함되어 있습니다.

**HTTP 상태 필터링에 대한 구성 설정을 편집하려면**

1. 데이터 집합 프로필 [!DNL Profile Manager] 내에서 파일을 열고 [!DNL Dataset\Log Processing\Traffic\HTTP Status Filter.cfg] 파일을 엽니다.

   >[!NOTE]
   >
   >구현을 사용자 정의한 [!DNL Site]경우 이러한 구성 설정이 있는 파일이 설명된 위치와 다를 수 있습니다.

1. 원하는 대로 파일의 매개 변수 값을 검토하거나 편집합니다. 다음 예를 안내서로 사용합니다.

   ![](assets/cfg_WebParameters_HTTPStatusFilter.png)

   조건에 대한 자세한 내용은 [!DNL Range] 조건을 [참조하십시오](../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md).

1. 창 맨 위에서 마우스 오른쪽 단추를 클릭하고 을 클릭하여 [!DNL HTTP Status Filter.cfg] 파일을 저장합니다 **[!UICONTROL (modified)]** . **[!UICONTROL Save]**

1. 로컬에서 변경한 내용을 적용하려면 열에서 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Profile Manager]> [!DNL User] &lt; **[!UICONTROL Save to]** > ***[!UICONTROL profile name]***&#x200B;을 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 데이터 세트에 포함된 파일이 속하는 상속된 프로필입니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.

## 로봇 필터링 {#section-7f43681dfbc64b969619cb88f97d5ad5}

조회 파일을 [!DNL Site] 사용하여 알려진 로봇에 의해 생성된 로그 항목, 테스트 스크립트 및 데이터 세트에서 내부 사용자에 대한 IP 주소를 제거하도록 구현을 구성할 수 있습니다. 기본 구현에는 로봇 필터링을 구성하는 [!DNL Log Processing Dataset Include] 파일이 포함되어 있습니다.

**로봇 필터링을 위한 구성 설정을 편집하려면**

1. 데이터 집합 프로필 [!DNL Profile Manager] 내에서 파일을 열고 [!DNL Dataset\Log Processing\Traffic\Robot Filter.cfg] 파일을 엽니다.

   >[!NOTE]
   >
   >구현을 사용자 정의한 [!DNL Site]경우 이러한 구성 설정이 있는 파일이 설명된 위치와 다를 수 있습니다.

1. 다음 예와 정보를 안내선으로 사용하여 파일의 매개 변수를 검토하거나 편집합니다.

   ![](assets/cfg_WebParameters_RobotFilter.png)

   파일에는 다음 세 가지 매개 변수로 정의된 [!DNL NotRobotCondition] 파일이 포함되어 있습니다.

   * **대/소문자 구분 로봇 필터링:** 참 또는 거짓 true이면 문자 대/소문자(위/아래)가 로봇 필터링에서 고려되지 않습니다.
   * **로봇 조회 파일, 기준:** 알려진 로봇이며 데이터 세트에서 필터링할 브라우저 사용자 에이전트 목록이 들어 있는 텍스트 파일의 경로와 파일 이름입니다. Adobe는 기본 로봇 조회 파일을 제공합니다. 경로를 지정하지 않으면 데이터 워크벤치 서버는 데이터 워크벤치 서버 설치 디렉토리 내의 조회 디렉토리에서 이 파일을 찾습니다.
   * **로봇 조회 파일, 확장:** 구현에 맞는 로봇을 정의하는 브라우저 사용자 에이전트 또는 IP 주소 목록이 포함된 선택적 텍스트 파일의 경로와 파일 이름입니다. 이 목록에는 내부 모니터링 로봇, 테스트 스크립트 및 데이터 세트에서 필터링해야 하는 내부 사용자에 대한 IP 주소가 포함될 수 있습니다. 경로를 지정하지 않으면 데이터 워크벤치 서버는 데이터 워크벤치 서버 설치 디렉토리 내의 조회 디렉토리에서 이 파일을 찾습니다.
   로그 항목의 브라우저 사용자 에이전트가 조회 파일에 나열되지 않으면 로그 항목은 실제 방문자가 생성한 것으로 간주되며 데이터 세트에서 필터링되지 않습니다.

   >[!NOTE]
   >
   >로봇 조회 파일에서 일치를 사용하면 하위 문자열을 사용하여 c-ip 및 cs(user-agent) 로그 필드와 비교합니다. 검색 문자열이 &quot;$&quot;로 시작하는 경우 테스트할 문자열의 앞과 일치해야 하며, &quot;$&quot;로 끝나는 경우 검색 문자열은 테스트되는 문자열의 끝과 일치해야 합니다. 검색 문자열이 &quot;$&quot;로 시작하고 끝나는 경우 문자열이 정확히 일치해야 로그 항목이 필터링됩니다. 예를 들어 클래스 C 블록의 모든 IP 주소를 테스트하려면 $231.78.123과 같은 문자열을 사용합니다.를 사용하여 문자열 앞면에 일치를 적용합니다. 이것은 주소 231.78.123.0 - 231.78.123.255와 일치합니다.

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭하여 파일을 저장합니다 **[!UICONTROL Save]**.

1. 로컬에서 변경한 내용을 적용하려면 열에서 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Profile Manager]> [!DNL User] &lt; **[!UICONTROL Save to]** > ***[!UICONTROL profile name]***&#x200B;을 클릭합니다. 여기서 프로필 이름은 데이터 세트 프로필의 이름이거나 데이터 세트에 포함된 파일이 속하는 상속된 프로필입니다.

   이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.

   >[!NOTE]
   >
   >데이터 집합을 구성하는 데 사용된 기본 로그 항목이 변경되지 않는 것이 중요한 경우(데이터 집합을 만들고 업데이트하는 데 사용된 변형 및 해당 크기가 변경된 경우에도), 로봇 조회 파일, 기준선 및 로봇 조회 파일, 확장 기능을 버전 제어해야 합니다. 이러한 파일에 버전 번호를 배치하면 기본 로봇 조회 파일 업데이트가 이러한 파일에서 항목을 추가하거나 삭제하여 이전에 생성된 보고 데이터 세트를 의도치 않게 변경하지 않습니다.

