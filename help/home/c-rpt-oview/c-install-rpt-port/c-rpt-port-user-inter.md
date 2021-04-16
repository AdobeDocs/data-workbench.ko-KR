---
description: 보고서 포털을 통해 올바르게 표시되는 보고서를 만들려면 보고서 세트를 특정 방법으로 구성해야 합니다.
title: 보고서 포털 사용자 인터페이스 사용자 지정
uuid: d1ea88e2-7b9e-4b1e-a826-dbe7c2e75976
exl-id: 1f7c807d-d896-448f-b9dd-9fe6a68ef27e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 2%

---

# 보고서 포털 사용자 인터페이스 사용자 지정{#customize-the-report-portal-user-interface}

보고서 포털을 통해 올바르게 표시되는 보고서를 만들려면 보고서 세트를 특정 방법으로 구성해야 합니다.

[!DNL Report Portal]의 사용자 인터페이스는 출력 디렉토리에 표시되고 [!DNL profiles.xml] 파일에 나열되는 각 보고서 세트 폴더에 대한 탭을 표시하도록 디자인되었으며, 이 탭은 표시할 [!DNL TopNavigation.xml] 파일에 추가해야 하는 내장 [!DNL Admin] 탭에 표시됩니다. 내장 [!DNL Admin] 탭을 표시하는 방법에 대한 자세한 내용은 [사용자의 탭에 출력 폴더 연결을 참조하십시오...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee).

![](assets/report_portal_home.png)

* [보고서 세트가 보고서 포털과 호환되는지 확인..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706)
* [출력 폴더를 사용자의 탭에 연결..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee)

## 보고서 세트가 보고서 포털 {#section-2b141e5d198a4bbea455699126c24706}과 호환하는지 확인

보고서 세트는 [!DNL Report]에 대한 예약된 작업을 정의합니다. 두 가지 항목으로 구성됩니다.

* [!DNL Report]에서 보고서로 생성할 작업 영역의 컬렉션을 정의하는 폴더.
* 구성 파일( [!DNL Report.cfg]).

무엇보다도 [!DNL Report.cfg] 파일은 [!DNL Report]에 보고서를 생성할 시기와 출력 파일을 저장할 위치를 알려줍니다. 보고서 세트는 데이터 워크벤치 서버의 보고서 폴더에 있습니다. 프로필에는 임의 개수의 보고서 세트가 표시될 수 있습니다.

[!DNL Report Portal]과(와) 호환되도록 보고서 세트는 다음 요구 사항을 충족해야 합니다.

* 보고서 세트의 출력 디렉토리에는 구성된 [!DNL profiles.xml] 파일이 있어야 합니다.
* 각 보고서 세트에는 &quot;*ReportSetName* Summary&quot;라는 최상위 보고서가 포함되어야 합니다. 여기서 *ReportSetName*&#x200B;은 보고서 세트 이름과 일치해야 합니다. 예를 들어 다음 [!DNL Profile Manager]에는 &quot;홈&quot; 및 &quot;트래픽&quot;이라는 두 개의 보고서 세트가 표시됩니다. 각 보고서 세트는 각각 [!DNL Home Summary.vw] 및 [!DNL Traffic Summary.vw] 요약 보고서를 정의합니다.

![](assets/rptPort_scrn_RptSets.png)

[!DNL Report Portal]에서 요약 보고서가 보고서 세트의 탭에 나타납니다. 요약 보고서에는 선택한 작업 공간, 창 또는 시각화가 포함될 수 있습니다.

* 요약 보고서는 보고서 세트의 최상위 수준 폴더에 있는 유일한 보고서여야 합니다. 다른 모든 보고서는 하위 폴더에 저장해야 합니다. 다른 보고서를 최상위 수준 폴더에 배치하는 경우 포털을 통해 볼 수 없습니다.

## 출력 폴더를 사용자 인터페이스 {#section-3f6bc47d37ed448e871f4f685f46acee}의 탭에 연결

[!DNL Report Portal]에 표시할 탭을 지정하려면 각 프로필에 대해 [!DNL TopNavigation.xml] 파일을 구성해야 합니다. 이 파일은 해당 탭의 순서와 특정 프로필에 대한 사용자 인터페이스에 탭으로 표시되는 보고서 세트를 결정합니다. [!DNL TopNavigation.xml] 파일은 \*PortalName*\PortalFiles\Core\TopNav\*profileName* 폴더에 있습니다.

**TopNavigation.xml 파일을 편집하려면**

1. IIS가 실행 중인 컴퓨터에서 메모장과 같은 텍스트 편집기에서 [!DNL TopNavigation.xml] 파일을 엽니다.
1. 다음 예제와 같이 [!DNL Report Portal] 출력을 표시할 보고서 세트의 이름 및 순서를 정의하도록 `<TopNav>` 요소 목록을 편집합니다.

   ```
   <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <TOPNAV_ELEMENTS>
   <TOPNAV>
       <NAME>Monthly Web</NAME>
     </TOPNAV>
     <TOPNAV>
       <NAME>Weekly Web</NAME>
     </TOPNAV>
   <TOPNAV> 
         <NAME>Admin</NAME> 
     </TOPNAV>
   </TOPNAV_ELEMENTS>
   ```

   >[!NOTE]
   >
   >[!DNL Admin] 탭은 추가 기능을 제공하는 내장 탭입니다. [!DNL TopNavigation.xml] 파일에 포함하지 않는 경우 이 탭은 표시되지 않으며 해당 기능을 사용할 수 없습니다.

1. \*PortalName*\PortalFiles\Core\TopNav\ folder에서 다음 프로필의 폴더를 만듭니다.
1. 첫 번째 프로필 폴더에서 [!DNL TopNavigation.xml] 파일을 복사하여 새 폴더에 붙여넣습니다.
1. 필요에 따라 [!DNL TopNavigation.xml]을(를) 편집한 다음 파일을 저장합니다.
1. 포털에서 사용 가능한 다른 모든 프로파일에 대해 3-5단계를 반복합니다.
