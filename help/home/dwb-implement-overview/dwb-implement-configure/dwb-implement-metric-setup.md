---
description: 이 섹션에서는 Data Workbench에서 지표를 만드는 방법을 설명합니다.
title: 지표 설정
uuid: 57c1410b-c09c-4a59-b3a1-575323e1b8e3
exl-id: a60c08d3-f708-43be-a14f-8b7f129f3ee5
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 3%

---

# 지표 설정{#metrics-setup}

이 섹션에서는 Data Workbench에서 지표를 만드는 방법을 설명합니다.

## 지표 이해 {#section-f0412e851fcb4ac9886dca4003d42cec}

지표는 보기 수, 주문 수, 수행된 호출 수 및 매출과 같은 고객 활동에 대한 수량 정보입니다. 지표는 보고서의 기초가 되며, 데이터 관계를 보고 이해하는 데 도움이 됩니다.

지표 Dimension을 사용하면 특정 수준별로 지표 수를 그룹화할 수 있습니다. 또한 특정 수준별로 지표 수를 그룹화할 수 있습니다.

## 새 지표 만들기 {#section-60a413899d1b4707965e06fb5ef7fc4e}

아래 절차에 따라 새 지표를 만드십시오.

1. **도구** > **지표 편집기**&#x200B;를 클릭합니다.

1. 지표 편집기에서 새 지표 이름과 공식을 입력합니다. ![](assets/dwb_impl_metrics1.png)

1. 지표 폴더에 저장합니다. ![](assets/dwb_impl_metrics2.png)

## 파생 지표 만들기 및 편집 {#section-ebdcd3ec652f485e90e001d694eab6d0}

지표 편집기를 사용하여 나중에 사용할 수 있도록 [!DNL User\profile_name\Metrics] 폴더에 저장된 이름, 공식 및 형식별로 새 지표를 정의합니다.

1. **관리 > 프로필** 메뉴 옵션을 사용하거나, 지표를 만들 폴더의 사용자 열을 마우스 오른쪽 단추로 클릭하고 **만들기 > 새 지표**&#x200B;를 클릭하여 새 지표 편집기를 엽니다. 지표 편집기가 표시됩니다.

1. *이름* 매개 변수에 새 지표의 이름을 입력합니다.

   >[!NOTE]
   >
   >공백( )은 사용할 수 있지만 밑줄(_)은 사용할 수 없습니다. 또한 다음 기호를 사용할 수 없습니다. + - * /

   ![](assets/dwb_impl_metrics3.png)

1. *공식* 매개 변수에 새 지표에 대한 표현식을 입력합니다.

   >[!NOTE]
   필터는 대괄호 [ 내에 정의해야 합니다 ] 를 입력합니다. 추가 지표 표현식 구문 규칙에 대해서는 [지표 표현식 구문](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)을 참조하십시오.

   이 표는 확장 지표에 대한 샘플 표현식을 제공합니다. ![](assets/dwb_impl_metrics4.png)

   >[!NOTE]
   적절한 표현식을 입력하면 미리 보기 라인에 새 지표의 값이 표시됩니다. 표현식에 오류가 있으면 미리 보기 라인에 오류 메시지가 표시됩니다.

1. 마우스 오른쪽 단추를 클릭하고 **저장**&#x200B;을 선택합니다. 지표를 저장하면 DWB *설치 디렉토리 \User\profile name\Metrics* 폴더에 새 지표를 나타내는 파일이 컴퓨터에 생성됩니다.

## 기존 파생 지표 편집 {#section-4b5b7baf885b45cc8b358d1bd774e925}

1. 프로필 관리자 또는 지표 관리자의 프로필 이름 열에서 편집할 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **로컬 만들기**&#x200B;를 클릭합니다.
1. 사용자 열에서 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 워크벤치에서 **열기**&#x200B;를 클릭합니다.

   >[!NOTE]
   시각화 내에서 지표 관련 영역을 마우스 오른쪽 단추로 클릭하여 지표 편집기를 열어 지표 메뉴를 표시할 수도 있습니다.

1. **지표 편집기**&#x200B;에서 *새 파생된 지표 만들기*&#x200B;의 단계 2-4를 사용하여 필요에 따라 지표 정의를 편집하고 저장합니다.

   프로필의 모든 사용자가 편집한 지표를 사용하도록 하려면 프로필 관리자를 사용하여 작업 프로필에 게시해야 합니다.

자세한 지원은 설명서를 참조하십시오.

[지표 표현식 구문](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)

[파생 지표 만들기 및 편집](https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/profile-mgr/c-drvd-mtrcs.html)
