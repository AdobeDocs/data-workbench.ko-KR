---
description: 보고서 포털을 통해 올바르게 표시되는 보고서를 만들려면 보고서 세트를 특정 방법으로 구성해야 합니다.
title: 보고서 포털 사용자 인터페이스 사용자 지정
uuid: d1ea88e2-7b9e-4b1e-a826-dbe7c2e75976
exl-id: 1f7c807d-d896-448f-b9dd-9fe6a68ef27e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 2%

---

# 보고서 포털 사용자 인터페이스 사용자 지정{#customize-the-report-portal-user-interface}

{{eol}}

보고서 포털을 통해 올바르게 표시되는 보고서를 만들려면 보고서 세트를 특정 방법으로 구성해야 합니다.

에 대한 사용자 인터페이스 [!DNL Report Portal] 출력 디렉토리에 표시되고 [!DNL profiles.xml] 파일 및 기본 제공 [!DNL Admin] 탭, [!DNL TopNavigation.xml] 표시할 파일입니다. 기본 제공 표시에 대한 자세한 내용 [!DNL Admin] 탭을 참조하십시오. [출력 폴더를 사용자의 탭에 연결..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee).

![](assets/report_portal_home.png)

* [보고서 세트가 보고서 포털과 호환되는지 확인..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706)
* [출력 폴더를 사용자의 탭에 연결..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee)

## 보고서 세트가 보고서 포털과 호환되는지 확인 {#section-2b141e5d198a4bbea455699126c24706}

보고서 세트는 다음에 대해 예약된 작업을 정의합니다 [!DNL Report]. 두 가지 항목으로 구성됩니다.

* 원하는 작업 영역의 컬렉션을 정의하는 폴더입니다 [!DNL Report] 를 보고서로 생성합니다.
* 구성 파일( [!DNL Report.cfg]).

특히, [!DNL Report.cfg] 파일 설명 [!DNL Report] 보고서를 생성할 시점 및 출력 파일을 저장할 위치. 보고서 세트는 Data Workbench 서버의 보고서 폴더에 있습니다. 프로필에는 원하는 개수의 보고서 세트가 표시될 수 있습니다.

와 호환되도록 하려면 [!DNL Report Portal]로 지정하는 경우, 보고서 세트는 다음 요구 사항을 충족해야 합니다.

* 보고서 세트의 출력 디렉터리에 구성된 항목이 있어야 합니다 [!DNL profiles.xml] 파일.
* 각 보고서 세트에는 라는 최상위 보고서가 포함되어야 합니다.*ReportSetName* 요약,&quot;위치 *ReportSetName* 는 보고서 세트의 이름과 일치합니다. 예를 들어, 다음 [!DNL Profile Manager] 에는 &quot;홈&quot;과 &quot;트래픽&quot;의 두 보고서 세트가 표시됩니다. 각 보고서 세트는 요약 보고서( [!DNL Home Summary.vw] 및 [!DNL Traffic Summary.vw])를 반환합니다.

![](assets/rptPort_scrn_RptSets.png)

in [!DNL Report Portal]요약 보고서가 보고서 세트의 탭에 표시됩니다. 요약 보고서에는 선택한 작업 공간, 창 또는 시각화가 포함될 수 있습니다.

* 요약 보고서는 보고서 세트의 최상위 폴더에 있는 유일한 보고서여야 합니다. 다른 모든 보고서는 하위 폴더에 배치해야 합니다. 다른 보고서를 최상위 폴더에 배치하는 경우 포털을 통해 볼 수 없습니다.

## 사용자 인터페이스의 탭에 출력 폴더 연결 {#section-3f6bc47d37ed448e871f4f685f46acee}

원하는 탭을 지정하려면 [!DNL Report Portal] 표시하려면 다음을 구성해야 합니다 [!DNL TopNavigation.xml] 각 프로필에 대한 파일입니다. 이 파일은 특정 프로필의 사용자 인터페이스에 탭으로 표시되는 보고서 세트와 해당 탭의 순서를 결정합니다. 다음 [!DNL TopNavigation.xml] 파일은 \*PortalName*\PortalFiles\Core\TopNav\*profileName* 폴더에 있습니다.

**TopNavigation.xml 파일을 편집하려면**

1. IIS가 실행 중인 컴퓨터에서 [!DNL TopNavigation.xml] 메모장과 같은 텍스트 편집기에 있는 파일입니다.
1. 목록 편집 `<TopNav>` 결과를 원하는 보고서 세트의 이름과 순서를 정의하기 위한 요소 [!DNL Report Portal] 다음 예와 같이 표시하려면 다음을 수행하십시오.

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
   >다음 [!DNL Admin] 탭은 추가 기능을 제공하는 내장 탭입니다. 에 포함하지 않는 경우 [!DNL TopNavigation.xml] 파일, 이 탭은 표시되지 않으며 해당 기능을 사용할 수 없습니다.

1. \*PortalName*\PortalFiles\Core\TopNav\ folder에서 다음 프로필에 대한 폴더를 만듭니다.
1. 를 복사합니다. [!DNL TopNavigation.xml] 첫 번째 프로필 폴더의 파일을 새 폴더에 붙여넣습니다.
1. 편집 [!DNL TopNavigation.xml] 필요에 따라 파일을 저장합니다.
1. 포털에서 사용할 수 있는 다른 모든 프로필에 대해 3~5단계를 반복합니다.
