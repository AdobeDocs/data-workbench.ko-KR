---
description: 보고서 서버 상태 및 보고서 세트 상태에 대한 정보입니다.
title: 보고서 상태 검토
uuid: 0f78a9fd-83d5-4e05-b7d1-d841033a5616
exl-id: a986f148-f019-457c-ade8-a4eaecbb1de7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 2%

---

# 보고서 상태 검토{#reviewing-report-status}

{{eol}}

보고서 서버 상태 및 보고서 세트 상태에 대한 정보입니다.

* [보고서 서버 상태](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-1a84f22439ee4a4ba2b3434e51e82ce0)
* [보고서 집합 상태](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-8569b94266b74a1f85d2a85106a2aaef)

## 보고서 서버 상태 {#section-1a84f22439ee4a4ba2b3434e51e82ce0}

**권장 빈도:** 필요한 경우에만

[!DNL Report] 는 상태 정보를 2분마다 Data Workbench 서버로 전송합니다 [!DNL Report] 서버. 이 정보는 [!DNL Report Server Status] 노드의 [!DNL Detailed Status] 인터페이스.

**를 열려면 [!DNL Detailed Status] 시각화**

1. Data Workbench에서 작업 공간을 마우스 오른쪽 단추로 클릭하고 를 클릭합니다. **[!UICONTROL Admin]** > **[!UICONTROL Servers]**.

1. 에서 [!DNL Servers] 인터페이스를 클릭한 다음, [!DNL Report] 에 연결된 후 클릭 **[!UICONTROL Detailed Status.]**

1. 클릭 **[!UICONTROL Report Server Status]**.

두 개 이상인 경우 [!DNL Report] 가 data workbench 서버에 연결되면 각각에 대한 항목이 표시됩니다 [!DNL Report Server] ( Status 벡터) 2분 간격은 [!DNL Reporting] 노드 [!DNL ReportServer.cfg] 파일.

에 대한 정보 [!DNL ReportServer.cfg] 파일, [보고서 집합 구성](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0). 구성에 대한 자세한 내용 [!DNL Report]를 참조하십시오. [보고서 설치](../../../home/c-rpt-oview/c-inst-rpt/c-inst-rpt.md#concept-3b8696a5b7f04ebfaafec7ff55890d91).

에 대한 자세한 정보 [!DNL Detailed Status]를 참조하려면 *Data Workbench 사용 안내서*.

## 보고서 집합 상태 {#section-8569b94266b74a1f85d2a85106a2aaef}

**권장 빈도:** 필요한 경우에만

[!DNL Report] Data Workbench 서버로 각 보고서 세트의 상태 정보를 전송합니다. 보고서 세트가 생성되는 시기 및 배포되는 위치와 같은 기본 정보는 보고서 세트 위의 Data Workbench에 녹색 텍스트로 표시됩니다. 보고서를 실행하는 동안 [!DNL Report] 서버는 현재 쿼리의 완료율을 나타내는 메시지를 2분마다 출력합니다. 이 2분 간격은 [!DNL Reporting] 노드 [!DNL ReportServer.cfg] 파일.

![](assets/report_status.png)

>[!NOTE]
>
>보고서를 실행하는 동안 오류가 발생하면 해당 보고서의 축소판 아래에 빨간색 텍스트로 오류가 표시됩니다. 작업 공간을 마우스 오른쪽 단추로 클릭하여 전체 오류 메시지를 표시할 수 있습니다.
