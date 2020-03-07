---
description: 보고서 세트를 보고서 포털을 통해 제대로 표시되는 보고서를 만들려면 특정 방법으로 구성해야 합니다.
solution: Analytics
title: 보고서 포털 사용자 인터페이스 사용자 지정
topic: Data workbench
uuid: d1ea88e2-7b9e-4b1e-a826-dbe7c2e75976
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 포털 사용자 인터페이스 사용자 지정{#customize-the-report-portal-user-interface}

보고서 세트를 보고서 포털을 통해 제대로 표시되는 보고서를 만들려면 특정 방법으로 구성해야 합니다.

의 사용자 인터페이스는 [!DNL Report Portal] 출력 디렉터리에 표시되고 파일에 나열되는 각 보고서 세트 폴더에 대한 탭과 표시할 파일에 추가해야 하는 기본 제공 [!DNL profiles.xml] 탭에 [!DNL Admin] [!DNL TopNavigation.xml] 표시되도록 설계되었습니다. 기본 제공 [!DNL Admin] 탭을 표시하는 방법에 대한 자세한 내용은 사용자 [탭에서 출력 폴더 연결을 참조하십시오.](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee).

![](assets/report_portal_home.png)

* [보고서 세트가 보고서 포털과 호환되는지 확인하는 중...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706)
* [출력 폴더를 사용자의 탭에 연결...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee)

## 보고서 세트가 보고서 포털과 호환되는지 확인 {#section-2b141e5d198a4bbea455699126c24706}

보고서 세트는 예약된 작업을 정의합니다 [!DNL Report]. 두 가지 항목으로 구성됩니다.

* 보고서로 생성할 작업 영역의 컬렉션을 정의하는 [!DNL Report] 폴더입니다.
* 구성 파일( [!DNL Report.cfg])입니다.

무엇보다도, 이 [!DNL Report.cfg] 파일은 보고서를 [!DNL Report] 생성할 시기와 출력 파일을 저장할 위치를 알려줍니다. 보고서 세트는 데이터 워크벤치 서버의 보고서 폴더에 있습니다. 프로필에는 보고서 세트 수를 표시할 수 있습니다.

호환되도록 [!DNL Report Portal]보고서 세트는 다음 요구 사항을 충족해야 합니다.

* 보고서 세트의 출력 디렉터리에 구성된 [!DNL profiles.xml] 파일이 있어야 합니다.
* 각 보고서 세트에는 &quot;ReportSetName *요약&quot;이라는* 최상위 보고서가 포함되어야 합니다. 여기서 *ReportSetName은* 보고서 세트의 이름과 일치해야 합니다. 예를 들어, 다음은 &quot;홈&quot; 및 &quot;트래픽&quot;이라는 두 개의 보고서 세트를 [!DNL Profile Manager] 보여줍니다. 각 보고서 세트는 요약 보고서( [!DNL Home Summary.vw] 및 [!DNL Traffic Summary.vw]각각)를 정의합니다.

![](assets/rptPort_scrn_RptSets.png)

에서 [!DNL Report Portal]요약 보고서가 보고서 세트의 탭에 나타납니다. 요약 보고서에는 선택한 작업 영역, 창 또는 시각화가 포함될 수 있습니다.

* 요약 보고서는 보고서 세트에 대한 최상위 폴더의 유일한 보고서여야 합니다. 다른 모든 보고서는 하위 폴더에 저장해야 합니다. 최상위 폴더에 다른 보고서를 배치하면 포털을 통해 볼 수 없습니다.

## 사용자 인터페이스의 탭에 출력 폴더 연결 {#section-3f6bc47d37ed448e871f4f685f46acee}

표시할 탭을 [!DNL Report Portal] 지정하려면 각 프로필에 대해 [!DNL TopNavigation.xml] 파일을 구성해야 합니다. 이 파일은 특정 프로필에 대한 사용자 인터페이스에 탭으로 표시되는 보고서 세트와 해당 탭의 순서를 결정합니다. 이 [!DNL TopNavigation.xml] 파일은 \*PortalName*\PortalFiles\Core\TopNav\*profileName* 폴더에 있습니다.

**TopNavigation.xml 파일을 편집하려면**

1. IIS가 실행 중인 컴퓨터에서 메모장과 같은 텍스트 편집기에서 [!DNL TopNavigation.xml] 파일을 엽니다.
1. 다음 예와 같이 출력물을 표시할 보고서 세트의 이름과 순서를 정의하도록 `<TopNav>` 요소 목록을 [!DNL Report Portal] 편집합니다.

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
   >이 [!DNL Admin] 탭은 추가 기능을 제공하는 내장 탭입니다. 파일에 포함하지 않는 경우 이 탭이 표시되지 않고 해당 기능을 사용할 수 없습니다. [!DNL TopNavigation.xml]

1. \*PortalName*\PortalFiles\Core\TopNav\ folder폴더에서 다음 프로필에 사용할 폴더를 만듭니다.
1. 첫 번째 프로필 폴더에서 파일을 복사하여 새 폴더에 붙여넣습니다. [!DNL TopNavigation.xml]
1. 필요에 따라 [!DNL TopNavigation.xml] 파일을 편집한 다음 저장합니다.
1. 포털에서 사용 가능한 다른 모든 프로필에 대해 3-5단계를 반복합니다.

