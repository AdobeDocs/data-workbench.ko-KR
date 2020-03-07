---
description: 이 섹션에서는 데이터 워크벤치에서 지표를 만드는 방법에 대해 설명합니다.
title: 지표 설정
uuid: 57c1410b-c09c-4a59-b3a1-575323e1b8e3
translation-type: tm+mt
source-git-commit: ded50c4eeadea80156c17a4cad985d0ceddd5500

---


# 지표 설정{#metrics-setup}

이 섹션에서는 데이터 워크벤치에서 지표를 만드는 방법에 대해 설명합니다.

## 지표 이해 {#section-f0412e851fcb4ac9886dca4003d42cec}

지표는 보기 수, 주문 수, 수행된 호출 수 및 매출과 같은 고객 활동에 대한 수량 정보입니다. 지표는 보고서의 기초가 되며, 데이터 관계를 보고 이해하는 데 도움이 됩니다.

지표 차원을 사용하면 특정 수준별로 지표 카운트를 그룹화할 수 있습니다. 또한 특정 수준별로 지표 카운트를 그룹화할 수 있습니다.

## 새 지표 만들기 {#section-60a413899d1b4707965e06fb5ef7fc4e}

아래 절차에 따라 새 지표를 만드십시오.

1. 도구 **>** 지표 **편집기를 클릭합니다**.

1. 지표 편집기에서 새 지표 이름과 공식을 입력합니다. ![](assets/dwb_impl_metrics1.png)

1. 지표 폴더에 저장합니다. ![](assets/dwb_impl_metrics2.png)

## 파생된 지표 만들기 및 편집 {#section-ebdcd3ec652f485e90e001d694eab6d0}

지표 편집기를 사용하여 이름, 공식 및 형식별로 새 지표를 정의하면 나중에 사용할 수 있도록 [!DNL User\profile_name\Metrics] 폴더에 저장됩니다.

1. 관리 > 프로필 **메뉴 옵션을 사용하거나** 지표를 만들 폴더의 사용자 열을 마우스 오른쪽 단추로 클릭하고 만들기 > 새 **지표를 클릭합니다**. 지표 편집기가 표시됩니다.

1. 이름 *매개* 변수에 새 지표의 이름을 입력합니다.

   >[!NOTE]
   >
   >공백()은 허용되고 밑줄(_)은 허용되지 않습니다. 또한 다음 심볼은 사용할 수 없습니다.+ - * /

   ![](assets/dwb_impl_metrics3.png)

1. 공식 *매개* 변수에서 새 지표에 대한 표현식을 입력합니다.

   >[!NOTE]
   필터를 대괄호 안에 정의해야 합니다. [ ] in the expression. 추가 지표 표현식 구문 규칙에 대해서는 지표 [표현식에 대한 구문을 참조하십시오.](https://docs.adobe.com/content/help/en/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)

   이 표에서는 확장 지표에 대한 샘플 표현식을 제공합니다. ![](assets/dwb_impl_metrics4.png)

   >[!NOTE]
   적절한 표현식을 입력하면 미리 보기 라인에 새 지표의 값이 표시됩니다. 식에 오류가 있으면 미리 보기 행에 오류 메시지가 표시됩니다.

1. 마우스 오른쪽 버튼을 클릭하고 저장을 **선택합니다**. 이 지표를 저장할 때 새 지표를 나타내는 파일이 DWB 설치 디렉토리 \User\profile name\Metrics 폴더에 사용자 컴퓨터에 *생성됩니다* .

## 기존 파생 지표 편집 {#section-4b5b7baf885b45cc8b358d1bd774e925}

1. 프로필 관리자 또는 지표 관리자의 프로필 이름 열에서 편집할 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [로컬로 만들기]를 **클릭합니다**.
1. 사용자 열에서 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **워크벤치에서 열기를** 클릭합니다.

   >[!NOTE]
   시각화 내에서 지표 관련 영역을 마우스 오른쪽 단추로 클릭하여 지표 편집기를 열어 지표 메뉴를 표시할 수도 있습니다.

1. 지표 **편집기에서**&#x200B;새 파생된 지표 만들기의 단계 2-4를 사용하여 필요에 따라 지표 *정의를 편집하고 저장합니다*.

   편집한 지표를 프로필의 모든 사용자가 사용하도록 하려면 프로필 관리자를 사용하여 작업 중인 프로필에 게시해야 합니다.

자세한 내용은 설명서를 참조하십시오.

[지표 표현식 구문](https://docs.adobe.com/content/help/en/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)

[파생된 지표 만들기 및 편집](https://docs.adobe.com/content/help/en/data-workbench/using/client/admin-ui/profile-mgr/c-drvd-mtrcs.html)
