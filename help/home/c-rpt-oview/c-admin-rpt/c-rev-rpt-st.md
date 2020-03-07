---
description: 보고서 서버 상태 및 보고서 세트 상태에 대한 정보입니다.
solution: Analytics
title: 보고서 상태 검토
topic: Data workbench
uuid: 0f78a9fd-83d5-4e05-b7d1-d841033a5616
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 상태 검토{#reviewing-report-status}

보고서 서버 상태 및 보고서 세트 상태에 대한 정보입니다.

* [보고서 서버 상태](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-1a84f22439ee4a4ba2b3434e51e82ce0)
* [보고서 세트 상태](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-8569b94266b74a1f85d2a85106a2aaef)

## 보고서 서버 상태 {#section-1a84f22439ee4a4ba2b3434e51e82ce0}

**권장 빈도:** 필요한 경우에만

[!DNL Report] 서버 상태와 관련하여 2분마다 데이터 워크벤치 서버에 상태 정보를 [!DNL Report] 보냅니다. 이 정보는 [!DNL Report Server Status] 인터페이스의 [!DNL Detailed Status] 노드 아래에 표시될 수 있습니다.

**시각화를 열려면[!DNL Detailed Status]**

1. 데이터 워크벤치에서 작업 영역을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Admin]** > **[!UICONTROL Servers]**&#x200B;을 클릭합니다.

1. 인터페이스에서 컴퓨터가 연결되는 데이터 워크벤치 서버 아이콘을 마우스 오른쪽 단추로 클릭하고 [!DNL Servers] [!DNL Report] 클릭합니다 **[!UICONTROL Detailed Status.]**

1. 클릭 **[!UICONTROL Report Server Status]**.

둘 이상의 항목이 데이터 워크벤치 서버에 [!DNL Report] 연결되어 있으면 상태 벡터에 각 항목에 [!DNL Report Server] 대한 항목이 나타납니다. 2분 간격은 파일 [!DNL Reporting] 노드의 상태 간격(초) 매개 변수에 값을 지정하여 재정의할 수 [!DNL ReportServer.cfg] 있습니다.

파일에 대한 자세한 내용은 보고서 [!DNL ReportServer.cfg] 세트 구성을 참조하십시오 [](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0). 구성에 대한 자세한 [!DNL Report]내용은 보고서 [설치를 참조하십시오](../../../home/c-rpt-oview/c-inst-rpt/c-inst-rpt.md#concept-3b8696a5b7f04ebfaafec7ff55890d91).

자세한 [!DNL Detailed Status]내용은 데이터 워크벤치 사용자 안내서의 관리 *인터페이스 장을 참조하십시오*.

## 보고서 세트 상태 {#section-8569b94266b74a1f85d2a85106a2aaef}

**권장 빈도:** 필요한 경우에만

[!DNL Report] 각 보고서 세트에 대한 상태 정보를 데이터 워크벤치 서버로 전송합니다. 보고서 세트가 생성되는 시기 및 배포되는 위치와 같은 기본 정보는 보고서 세트 위의 데이터 워크벤치에 녹색 텍스트로 표시됩니다. 보고서를 실행하는 동안 [!DNL Report] 서버는 현재 쿼리의 완료 비율을 나타내는 메시지를 2분마다 출력합니다. 이 2분 간격은 파일 [!DNL Reporting] 노드의 완료 메시지 간격(초) 매개 변수에 값을 지정하여 재정의할 수 [!DNL ReportServer.cfg] 있습니다.

![](assets/report_status.png)

>[!NOTE]
>
>보고서를 실행하는 동안 오류가 발생하면 해당 보고서의 축소판 아래에 빨간색 텍스트로 오류가 표시됩니다. 작업 영역을 마우스 오른쪽 단추로 클릭하여 전체 오류 메시지를 표시할 수 있습니다.
