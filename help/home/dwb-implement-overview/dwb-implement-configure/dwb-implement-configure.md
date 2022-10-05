---
description: DWB 구성 및 구현에 대한 설명서입니다.
title: Data Workbench 구성 및 구현
uuid: a6f55cb5-c348-419c-9d21-c3fe608d4ab6
exl-id: ac9df711-0cce-46d3-8a44-a34a4deaf3c7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 3%

---

# Data Workbench 구성 및 구현{#data-workbench-configuration-and-implementation}

{{eol}}

DWB 구성 및 구현에 대한 설명서입니다.

* 대상 **데이터 처리 - 기본 키 작성**&#x200B;를 참조하십시오. [이벤트 데이터 레코드](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/c-ev-data-rec-fields.html) 및 [기본 키 작성](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-primary-key.md#concept-04e756573bf14d8e953a983e209290bd).

* 대상 **데이터 처리 - 이벤트 시간 설정**&#x200B;를 참조하십시오. [이벤트 데이터 레코드](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/c-ev-data-rec-fields.html) 및 [이벤트 시간 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-event-time.md#concept-7f84404b57e54d879411621660d20708).

* 대상 **데이터 처리 - Dimension 설정**&#x200B;를 참조하십시오. [확장 Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/c-abt-ex-dim.html) 및 [Dimension 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-dim-setup.md#concept-cf6e1e55038042c3ac3ae5921316538f).

* 대상 **데이터 처리 - 지표 설정**&#x200B;를 참조하십시오. [지표 설명](https://experienceleague.adobe.com/docs/analytics/components/variables/metrics/metricslist.html) 및 [지표 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-metric-setup.md#concept-f568a931db5b4b62b7b1e7827c7f7bf6).

* 대상 **액세스 제어의 클러스터 멤버**&#x200B;를 참조하십시오. [액세스 제어 구성](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/admin-dwb-server/access-control/c-config-acs-ctrl.html).

* 대상 **프로필 구성 파일의 처리 서버**&#x200B;를 참조하십시오. [클러스터에서 실행할 프로필 구성](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/install-servers/insight-server-clusters/install-insight-server-cluster/c-config-prof-run-clstr.html).

* 종료 **세그먼트 내보내기 설정**&#x200B;를 참조하십시오. [세그먼트 내보내기를 사용하여 데이터 내보내기](https://experienceleague.adobe.com/docs/data-workbench/using/client/export-data/c-exp-data-seg-exp.html).

* 종료 **표준화 서버 설정**&#x200B;를 참조하고 [파일 서버 구성 프로세스](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/log-proc-config-file/c-ins-svr-file-svr-unit.html).

* 종료 **주소 파일에서 클러스터 멤버 설정**&#x200B;를 참조하고 [Insight Server에 설치된 주소 파일](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/install-servers/insight-server-dpu/server-network-location/c-addr-file-inst.html).

* 대상 **내부 및 외부 FTP 설정 유효성 검사**&#x200B;를 참조하십시오. [FTP 서버 유효성 검사](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-validation-ftp.md#concept-8b677e0581c1490ebfbefdbedaf28d54).

* 종료 **이전 날짜에 대한 데이터 피드 일관성 확인**&#x200B;를 참조하십시오. [내역 데이터 피드 유효성 확인](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-datafeeds-historical.md#concept-03639f41b5944a018095b467e6a08b4b).

* 종료 **주간 재처리 로그 설정 및 스케줄로 설정**&#x200B;를 참조하십시오. [주간 재처리로 스크립팅](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-reprocess-scripting.md#concept-60529e12d6d94386a02c1c6fdedf0295).

* 종료 **SAINT Scrubber에 대한 스크립팅 설정**&#x200B;를 참조하십시오. [SAINT Scrubber용 스크립팅](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-saint-scripting.md#concept-8631931cd7f14d64a97c426f3bc7a076).

* 대상 **보고서 서버 설정**&#x200B;를 참조하십시오. [DWB 보고서 서버 설정](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-qry-lang-syntx.html).

* 대상 **기본 DWB 쿼리 API 설정 지침**&#x200B;를 참조하십시오. [쿼리 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-query-api.md#concept-94a135c593fe47dcb2f1e06abab6c78b).

* 대상 **기본 DWB 쿼리 API 설정 구문**&#x200B;를 참조하십시오. [쿼리 언어](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-qry-lang-syntx.html).
