---
description: Data Workbench 6.7의 새로운 기능, 수정 내용 및 알려진 문제
title: Data Workbench 6.7 릴리스 정보
uuid: b84f5f2b-4f1c-490c-982b-6bd8d3a63e25
exl-id: e5ec3224-66d1-47a6-9bf3-8be9f6568b8d
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 34%

---

# Data Workbench 6.7 릴리스 정보{#data-workbench-release-notes}

Data Workbench 6.7의 새로운 기능, 수정 내용 및 알려진 문제

## Data Workbench 6.7 릴리스 정보 {#topic-7655534554ac4a4b816af1bd73b06aad}

Data Workbench 6.7의 새로운 기능, 수정 내용 및 알려진 문제

## 릴리스 6.7의 새로운 기능 {#section-8bd7a36ac3a24b8497a9ea9724e0d750}

**Data Workbench 워크스테이션의 새 인증 모델(IMS 통합)**

Data Workbench 워크스테이션은 이제 사용자 이름과 암호를 통해 사용자 인증을 지원합니다. 이 새로운 방법을 통해 관리자는 자신의 사용자 계정을 만들고 관리할 수 있으므로, 고객 지원에 문의할 필요가 없습니다.

자세한 내용은 [사용자의 자체 프로비저닝](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-self-provisioning-users.html)을 참조하십시오.

**플랫 파일 조회**

Data Workbench 워크스테이션은 이제 사용자 이름과 암호를 통해 사용자 인증을 지원합니다. 이 새로운 방법을 통해 관리자는 자신의 사용자 계정을 만들고 관리할 수 있으므로, 고객 지원에 문의할 필요가 없습니다.

플랫 파일 조회는 이전에 전체 파일을 메모리 내 버퍼에 로드했기 때문에 메모리 사용이 늘어나며 다른 하위 시스템의 성능 문제가 발생했습니다. 이제 Windows에서 파일을 메모리 매핑하고 캐시할 수 있으므로, **&#x200B;에서 Memory Mapped Lookup Files를 [!DNL MemorySettings.cfg]true로 설정하여 메모리 사용을 최적화할 수 있습니다 .

자세한 내용은 [사용자의 자체 프로비저닝](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-self-provisioning-users.html)을 참조하십시오.

**메모리 사용**

[!DNL MemorySettings.cfg]에서 *큰 페이지 사용*&#x200B;을 false로 설정하여 큰 페이지 사용을 비활성화할 수 있습니다. 자세한 내용은 [메모리 사용 모니터링](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/admin-dwb-server/t-mntr-mry-usg.html)을 참조하십시오.

**보안 암호**

ECDHE 및 DHE에 대한 지원이 추가되었습니다.

[!DNL User List.cfg]에서 이메일 지원

[!DNL User List.cfg]에 이메일 특성에 대한 지원이 추가되었습니다. 자세한 내용은 [그룹 구성원의 사용자 관리](https://docs.adobe.com/help/en/data-workbench/using/server-admin-install/admin-dwb-server/access-control/dwb-self-admin-member-access.html)를 참조하십시오.

**도움말 메뉴**

이제 도움말 메뉴에 Open Certificates 디렉토리에 대한 바로 가기가 표시됩니다.

**`TargetBulkUpload`내보내기**

중단된 배치 기록을 추적하기 위해 `targetbulkuploadexportname.log.completed` 파일과 내보내기 추적 파일의 끝 부분에 URL이 제공됩니다.

최대 시간 제한 간격(분)을 구성하기 위해 새 파일인 [!DNL TargetBulkUpload.cfg]가 제공되었습니다. 이 파일은 [!DNL Server\Admin\Export\]에 있습니다.

## 수정 사항 {#section-160baf6ea04c45a993777ee4260691ed}

* 캠페인 클릭스루 차원에 부풀려진 값이 표시되는 문제가 수정되었습니다.
* 보고서 서버에서 excel 파일을 생성하는 문제를 해결했습니다.
* 이제 RC4 암호화는 기본적으로 비활성화됩니다.
* 값 범례 테이블에 차원 요소를 추가할 때 Data Workbench 워크스테이션이 충돌하는 문제를 해결했습니다.
* AAM 내보내기 Data Workbench에서 시간 초과를 초래하는 문제를 수정했습니다.
* 충분한 액세스 수준 없이 사용자가 작업 공간을 서버에 저장할 때 Data Workbench 워크스테이션이 충돌하는 문제를 해결했습니다.
* [!DNL report.cfg]의 날짜 형식이 잘못되었거나 현지화되지 않는 문제를 수정했습니다.
* AVRO 피드의 모바일 및 제품 행에 혼용 정보가 표시되는 문제를 해결했습니다.
* [!DNL order.txt]에서 `*.1cd` 및 `*.1ad` 파일을 정렬할 수 없는 문제를 해결했습니다.

* 클러스터링을 실행하는 동안 예상 최대 알고리즘에 대해 [서버에 제출] 옵션을 사용할 수 없습니다.
* `TargetBulkUpload` 실행 가능한 지연 및 완전히 실행되지 않는 문제를 해결했습니다.

## 알려진 문제 {#section-d76322bdac5043f087ab303dc68b8fff}

* 로그아웃하면 [!DNL user cache.db] 파일이 정리됩니다.
* &#39;+&#39; 또는 &#39;%&#39; 문자가 포함된 IMS 사용자 이메일 주소는 지원되지 않습니다.
* 연결 상태의 오류 중에 사용자가 로그아웃할 수 없습니다. 해결 방법으로, 오프라인 모드에서 로그아웃합니다.
* 해상도와 DPI가 높은 일부 하드웨어에 IMS 로그인 창이 제대로 렌더링되지 않습니다. 해결 방법으로, [!DNL Insight.exe] 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Properties]** > **[!UICONTROL Compatability]** 로 이동한 다음, **[!UICONTROL Override high DPI scaling behavior]** 상자를 선택합니다.

## 업그레이드 요구 사항 {#section-b74adf981ac8446a8d7ffcdc4e9cf939}

1. 빌드 패키지의 일부인 Insight Server에서 [!DNL trust_ca_cert.pem]을 업데이트합니다.
1. [https://aap.adobe.com](https://aap.adobe.com)에서 새 인증서를 다운로드하여 서버 및 보고서 서버의 인증서를 업데이트합니다.
1. 워크스테이션 및 보고서 서버를 자동으로 업데이트하려면 라이센스 서버에서 두 워크스테이션 모두에 대해 [!DNL trust_ca_cert.pem]을(를) 다운로드하여 수동으로 업데이트하십시오.
1. 센서의 자동 업데이트 기능을 사용하려면 Insight Server 버전 6.70과 통신하기 위해 버전 5.0이 필요합니다. 또한 라이센스 서버에서 센서를 다운로드하여 센서의 [!DNL trust_ca_cert.pem]을 수동으로 업데이트해야 합니다.

## 시스템 업데이트 {#section-c1b4949ea734440aa62658ac313261db}

새 파일은 다음과 같습니다.

1. [!DNL Server\Admin\Export\TargetBulkUpload.cfg]
1. [!DNL Server\Components for Processing Servers\MemorySettings.cfg]
1. [!DNL Server\Components\MemorySettings.cfg]

업데이트된 파일은 다음과 같습니다.

1. [!DNL trust_ca_cert.pem] 모든 구성 요소에 사용할 수 있습니다.
1. [!DNL Access Control.cfg] IMS 구성을 지원합니다.
1. [!DNL Base\Context\meta.cfg] 지원 시작 날짜 및 종료 날짜 형식  [!DNL Report.cfg]

1. IMS 인증에 대한 프록시를 지원하기 위해 [!DNL Insight.cfg]에 추가합니다.

   ```
   IMS Proxy Info = IMSProxyInfo: 
     Proxy Password = EncryptedString:
     Proxy User Name = string:
   ```

5.3~5.52에 대해서는 [보관된 릴리스 노트](https://experienceleague.adobe.com/docs/data-workbench/using/release-notes/release-notes.html)를 참조하십시오.
