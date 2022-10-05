---
description: 다음 단계에 따라 Data Workbench v6.5로 업그레이드하십시오.
title: 6.4에서 6.5로 업그레이드
uuid: b90b7b0c-7467-405f-a5ca-c40e69975d49
exl-id: bcfd1ab1-2fb8-4bcd-b6c9-329143274ca4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# 6.4에서 6.5로 업그레이드{#upgrading-to}

{{eol}}

다음 단계에 따라 Data Workbench v6.5로 업그레이드하십시오.

## 업그레이드 요구 사항 및 Recommendations {#section-8704a9ac358246cd81233dd0982d534f}

Data Workbench 6.5로 업그레이드할 때 이러한 요구 사항과 권장 사항을 따르십시오.

* 의 변경 사항 **[!DNL Components for Processing Servers\Communications.cfg]** 파일을 사용하려면 DWB 6.5 릴리스에 대해 이 파일을 업데이트해야 합니다. 다음 *SourceListServer*, *SegmentExportServer*, 및 *정규화 서버* 항목이 제거되었습니다. ( DPU가 실행되고 있지 않아야 함) *sourcelist*, *세그먼트 내보내기*, 또는 *서버 정규화*. )

* 상관 관계 코드, 상관 관계 매트릭스, 연결 코드, 연결 매트릭스, 성향 점수 및 최적 속성 시각화는 이제 다중 패스 시각화입니다.

   작업 공간에 다중 전달 시각화가 두 개 이상 있는 경우 보고서 서버가 기본적으로 오류로 인해 보고서를 생성하지 못합니다.

   ```
   Too many Multipass visualizations in workspace ....... (has #, 1 allowed).
   ```

   을 업데이트하여 이 오류를 방지합니다. [!DNL ReportServer.cfg] 파일을 만들거나 기존 파일에 이 줄을 추가합니다. *보고* 섹션을 참조하십시오.

   ```
   Max Multipass Per Slice = int: n
   ```

   여기서 n은 작업 공간에서 보고서 서버가 지원하는 최대 다중 전달 시각화 수입니다.
