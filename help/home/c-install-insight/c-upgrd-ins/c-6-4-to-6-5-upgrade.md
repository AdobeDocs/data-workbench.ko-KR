---
description: 다음 단계에 따라 Data Workbench v6.5로 업그레이드하십시오.
title: 6.4에서 6.5로 업그레이드
uuid: b90b7b0c-7467-405f-a5ca-c40e69975d49
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Upgrading 6.4 to 6.5{#upgrading-to}

다음 단계에 따라 Data Workbench v6.5로 업그레이드하십시오.

## 업그레이드 요구 사항 및 권장 사항 {#section-8704a9ac358246cd81233dd0982d534f}

Data Workbench 6.5로 업그레이드할 때 다음 요구 사항 및 권장 사항을 따르십시오.

* 파일의 변경 내용을 적용하려면 DWB 6.5 릴리스에 대해 이 파일을 업데이트해야 합니다. **[!DNL Components for Processing Servers\Communications.cfg]** SourceListServer *,* SegmentExportServer *및* NormalizeServer *항목이제거되었습니다* . ( DPU는 *소스*, *세그먼트 내보내기*&#x200B;또는 *서버*&#x200B;표준화를실행하지 않아야 합니다.)

* 상관 관계 코드표, 상관 관계 매트릭스, 연결 코드표, 연관 매트릭스, 성향 점수 및 최적 속성 시각화는 이제 다중 패스 시각화입니다.

   한 작업 공간에 다중 패스 시각화가 두 개 이상 있을 경우, 보고서 서버가 기본적으로 보고서를 생성하지 못합니다. 오류:

   ```
   Too many Multipass visualizations in workspace ....... (has #, 1 allowed).
   ```

   이 오류는 [!DNL ReportServer.cfg] 파일을 업데이트하거나 보고 섹션의 기존 파일에 이 줄을 추가하면 *되지* 않습니다.

   ```
   Max Multipass Per Slice = int: n
   ```

   여기서 n은 작업 공간에서 보고서 서버가 지원하는 다중 패스 시각화의 최대 수입니다.

