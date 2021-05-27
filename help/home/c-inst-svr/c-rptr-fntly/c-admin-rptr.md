---
description: 반복 기능을 위한 관리 작업은 Insight Server의 관리 작업과 매우 유사합니다.
title: 반복 관리
uuid: 4fbfce3a-2610-4dcd-a585-cb7ee07b90db
exl-id: 5c7a4f95-be4b-4c2c-8dea-19037ba0b5cc
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 12%

---

# 반복 관리{#administering-repeater}

반복 기능을 위한 관리 작업은 Insight Server의 관리 작업과 매우 유사합니다.

다음 관리 작업이 적용됩니다.[!DNL Insight Server] DPU를 반복 서버와 함께 사용할 수 있도록 각 단계 이후에 수행해야 하는 예외 또는 변경 사항입니다.

* [디지털 인증서 유효성 재확인](../../../home/c-inst-svr/c-admin-inst-svr/c-reval-dgtl-cert.md#concept-f0020a6f0d6f477099b7a8f0b6e2944c)
* [서비스가 실행 중인지 확인](../../../home/c-inst-svr/c-admin-inst-svr/c-cfrm-svc-rng.md#concept-15b046e92d254bbd95dec829abc76677) 서비스 제어판의 서비스 목록에서 &quot;반복&quot;을 찾습니다.

* [액세스 제어 구성](../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d)
* [디스크 ](../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/c-mntr-disk-spc.md#concept-a83447e44f4e47aba282328be395a0d4) 공간 모니터링반복 서버에 적용되는 데이터 유형은 이벤트, 운영 체제 및 시스템 데이터입니다. 백업 스토리지에 반복 서버를 사용하는 경우 시스템에서 더 많은 데이터 저장 공간을 사용할 수 있도록 해야 하는 경우, 최신 로그 파일을 제외한 모든 파일을 다른 시스템 또는 데이터 저장 매체(zip 드라이브, 테이프 등)로 이동할 수 있습니다. 데이터를 이동해도 반복 서비스를 중지할 필요가 없습니다.

   >[!NOTE]
   >
   >중계기에서 삭제하기 전에 [!DNL .vsl] 파일의 백업 사본의 무결성을 확인해야 합니다.

* [관리 경고 구성](../../../home/c-inst-svr/c-admin-inst-svr/t-config-adm-alrts.md#task-0858f588da4941aa9d4952f6592681aa)
* [관리 이벤트 모니터링](../../../home/c-inst-svr/c-admin-inst-svr/t-mntr-adm-evts.md#task-4c78325b3e6e4dde8fa94c1896e19e34)
* [감사 로그 모니터링](../../../home/c-inst-svr/c-admin-inst-svr/t-mntr-adt-lgs.md#task-5dd9830424fe440ea1369215a1aca231)
* [통신 구성](../../../home/c-inst-svr/c-admin-inst-svr/t-config-com.md#task-471305ecf7a644789a288f93c42514ec)
* [서비스 기능](../../../home/c-inst-svr/c-admin-inst-svr/t-rest-svc.md#task-97f97f1019bc440080ab2fddfdc04c74)  [!DNL Repeater] 을 다시 시작하는 것은 계속 실행되도록 설계되었습니다. 시스템을 다시 시작하면 반복기가 자동으로 다시 시작됩니다. 수동으로 반복을 시작하고 중지해야 하는 경우 Windows의 서비스 제어판에서 다시 시작할 수 있습니다.
