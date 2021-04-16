---
description: 기존 사용자 계정을 편집하는 절차.
title: 기존 사용자 편집
uuid: 5c01f0f9-0d30-4526-a4fb-43c7e1cb076f
exl-id: cfbc54d8-16b4-4629-b556-a2aa4ee0c606
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 3%

---

# 기존 사용자 편집{#editing-existing-users}

기존 사용자 계정을 편집하는 절차.

1. [!DNL Report Portal]에서 **[!UICONTROL Admin]** 탭을 클릭합니다. [!DNL Admin] 페이지가 나타납니다.

   ![](assets/report_admintag2.png)

1. 편집할 계정 이름의 첫 번째 문자를 나타내는 문자를 클릭합니다. 예를 들어 &quot;Marketing&quot; 계정을 편집하려면 &quot;M&quot;이라는 문자를 클릭합니다.

   해당 문자로 시작하는 계정 이름 목록이 표시됩니다.

1. 편집할 계정 이름을 선택한 다음 **[!UICONTROL select]** 단추를 클릭합니다. [!DNL Edit Account Info] 페이지가 나타납니다.

   ![단계 정보](assets/rptPort_scrn_AdminTab_editUser.png)

1. 이 페이지에서 업데이트해야 하는 필드만 변경합니다. 다음 표에서는 이러한 각 필드에 대해 설명합니다.

   | 이 필드에서... | 분류에 사용할 . . . |
   |---|---|
   | 이메일 | 사용자의 이메일 주소입니다. |
   | 이전 암호 | 관리자 계정을 편집하거나 관리자가 아닌 계정의 암호를 재설정할 때 계속 진행해야 하는 현재 암호입니다. |
   | 새 암호 | [!DNL Report Portal]에 로그인할 때 사용자가 제공해야 하는 새 암호입니다. |
   | 암호 확인 | [!DNL Report Portal]에 로그인할 때 사용자가 제공해야 하는 새 암호입니다. |
   | 프로파일 액세스 | 이 사용자가 액세스할 수 있는 프로필(예: ProductSales). 여러 프로필에 액세스할 수 있도록 하려면 쉼표로 이름을 구분합니다. 사용자가 [!DNL Report Portal]과(와) 연관된 모든 프로파일에 액세스할 수 있는 경우 &quot;ALL&quot;을 입력합니다. |
   | 탭 액세스 | 이 사용자가 액세스할 수 있는 탭(예: [!DNL Admin]). 여러 탭에 대한 액세스를 허용하려면 이름을 쉼표로 구분합니다. 사용자가 [!DNL Report Portal]의 모든 탭에 액세스할 수 있는 경우 &quot;ALL&quot;을 입력합니다. 이 필드는 계정 유형 필드와 함께 그룹 액세스 권한을 정의하는 데 매우 유용합니다. |
   | 계정 유형 | 이 계정이 개인 계정인지 그룹 계정인지 여부입니다. 개별 계정을 사용하면 사용자가 암호를 재설정할 수 있지만 그룹은 암호를 재설정할 수 없습니다. 관리자는 그룹 계정의 암호를 재설정할 수 있는 유일한 사람입니다. |
   | status | 이 계정이 활성 상태인지 비활성 상태인지 여부입니다. 기본값은 활성 상태입니다. 사용자 계정을 비활성화하려면 **[!UICONTROL inactive]**&#x200B;을 선택합니다. |
   | 관리 | 이 사용자가 각 보고서와 관련된 메모를 편집할 수 있을 뿐만 아니라 사용자 계정을 만들고, 업데이트하고 삭제할 수 있도록 허용할지 여부. 기본 설정은 false입니다. 이 사용자를 관리자 사용자로 만들려면 true를 선택합니다. |
   | 만료 날짜 | 이 사용자가 [!DNL Report Portal]을(를) 사용할 수 있을 때까지 MM/DD/YYYY 형식의 날짜입니다. |

1. 클릭 **[!UICONTROL update]**.
