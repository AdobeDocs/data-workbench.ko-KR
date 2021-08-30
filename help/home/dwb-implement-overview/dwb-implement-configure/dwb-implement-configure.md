---
description: DWB 구성 및 구현에 대한 설명서입니다.
title: Data Workbench 구성 및 구현
uuid: a6f55cb5-c348-419c-9d21-c3fe608d4ab6
exl-id: ac9df711-0cce-46d3-8a44-a34a4deaf3c7
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 3%

---

# Data Workbench 구성 및 구현{#data-workbench-configuration-and-implementation}

DWB 구성 및 구현에 대한 설명서입니다.

* **데이터 처리 - 기본 키**&#x200B;를 빌드하려면 [이벤트 데이터 레코드](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/c-ev-data-rec-fields.html) 및 [기본 키 작성](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-primary-key.md#concept-04e756573bf14d8e953a983e209290bd)을 참조하십시오.

* **데이터 처리 - 이벤트 시간 설정**&#x200B;에 대해서는 [이벤트 데이터 레코드](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/c-ev-data-rec-fields.html) 및 [이벤트 시간 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-event-time.md#concept-7f84404b57e54d879411621660d20708)을 참조하십시오.

* **데이터 처리 - Dimension 설정**&#x200B;에 대해서는 [확장 Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/c-abt-ex-dim.html) 및 [Dimension 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-dim-setup.md#concept-cf6e1e55038042c3ac3ae5921316538f)을 참조하십시오.

* **데이터 처리 - 지표 설정**&#x200B;에 대해서는 [지표 설명](https://experienceleague.adobe.com/docs/analytics/components/variables/metrics/metricslist.html) 및 [지표 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-metric-setup.md#concept-f568a931db5b4b62b7b1e7827c7f7bf6)을 참조하십시오.

* **Cluster Members in Access Control**&#x200B;의 경우 [Configuring Access Control](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/admin-dwb-server/access-control/c-config-acs-ctrl.html)을 참조하십시오.

* 프로필 구성 파일의 **처리 서버**&#x200B;에 대해서는 [클러스터에서 실행할 프로필 구성](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/install-servers/insight-server-clusters/install-insight-server-cluster/c-config-prof-run-clstr.html)을 참조하십시오.

* **세그먼트 내보내기 설정**&#x200B;하려면 [세그먼트 내보내기를 사용하여 데이터 내보내기](https://experienceleague.adobe.com/docs/data-workbench/using/client/export-data/c-exp-data-seg-exp.html)를 참조하십시오.

* **정규화 서버 설정**&#x200B;하려면 [파일 서버 구성 프로세스](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/log-proc-config-file/c-ins-svr-file-svr-unit.html)를 참조하십시오.

* 주소 파일&#x200B;**에서**&#x200B;클러스터 구성원을 설정하려면 Insight Server](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/install-servers/insight-server-dpu/server-network-location/c-addr-file-inst.html)에 설치된 [주소 파일을 참조하십시오.

* **내부 및 외부 FTP에 대한 유효성 검사 설정**&#x200B;에 대해서는 [FTP 서버 유효성 검사](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-validation-ftp.md#concept-8b677e0581c1490ebfbefdbedaf28d54)를 참조하십시오.

* **이전 날짜에 대한 데이터 피드의 일관성 검사를 수행하려면 [이전 데이터 피드 유효성 확인](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-datafeeds-historical.md#concept-03639f41b5944a018095b467e6a08b4b)을 참조하십시오.**

* **주간 재처리 로그를 설정하고 예약하려면 [주간 재처리로 스크립팅](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-reprocess-scripting.md#concept-60529e12d6d94386a02c1c6fdedf0295)을 참조하십시오.**

* **SAINT Scrubber**&#x200B;에 대한 스크립팅을 설정하려면 [SAINT Scrubber](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-saint-scripting.md#concept-8631931cd7f14d64a97c426f3bc7a076)에 대한 스크립팅 을 참조하십시오.

* **보고서 서버 설정**&#x200B;에 대해서는 [DWB 보고서 서버 설정](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-qry-lang-syntx.html)을 참조하십시오.

* **기본 DWB 쿼리 API 설정 지침**&#x200B;에 대해서는 [쿼리 설정](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-query-api.md#concept-94a135c593fe47dcb2f1e06abab6c78b)을 참조하십시오.

* **기본 DWB 쿼리 API 설정 구문**&#x200B;에 대해서는 [쿼리 언어](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-qry-lang-syntx.html)를 참조하십시오.
