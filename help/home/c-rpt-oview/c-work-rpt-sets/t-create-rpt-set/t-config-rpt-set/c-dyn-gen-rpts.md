---
description: 조회 파일에서 지정하는 차원 요소나 주문 수가 10개 가장 많은 사용자와 같이 특정 수의 차원 요소에 대해 동적으로 보고서를 생성할 수 있습니다.
solution: Analytics
title: 동적으로 보고서 생성
topic: Data workbench
uuid: 87174fb5-e72f-4758-8e9d-1aaa784c1898
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 동적으로 보고서 생성{#dynamically-generating-reports}

조회 파일에서 지정하는 차원 요소나 주문 수가 10개 가장 많은 사용자와 같이 특정 수의 차원 요소에 대해 동적으로 보고서를 생성할 수 있습니다.

>[!NOTE]
>
>Adobe는 일별(또는 더 자주) 보고서 생성을 위한 동적 보고서 세트 생성을 제한합니다. 큰 쿼리 또는 복잡한 쿼리를 사용하여 보고서를 구성하는 경우 동적 보고서 생성은 리소스를 많이 사용할 수 있습니다.

* [조회 파일 차원 요소 보고서](../../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-dyn-gen-rpts.md#section-a5e8f38af06c42b4bfddec4bafbf03d6)
* [상위 차원 요소 보고서](../../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-dyn-gen-rpts.md#section-d8d75a6dfadd407bb18d6f32d70ebf8f)

## 조회 파일 차원 요소 보고서 {#section-a5e8f38af06c42b4bfddec4bafbf03d6}

조회 파일에 지정된 차원의 요소에 대해 보고서를 동적으로 생성하고(선택 사항) 배포하도록 보고서 세트를 구성하려면 [!DNL Report.cfg] 파일에 다음 매개 변수를 지정합니다.

* [!DNL Dimension Name]
* [!DNL Lookup File]

이러한 매개 변수에 대한 자세한 내용은 Report.cfg [매개 변수를 참조하십시오](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

**조회 파일을 사용하여 동적 보고서 세트를 만들려면**

1. 주어진 차원에 대해 두 열 조회 파일을 만듭니다. 이 파일에는 두 개의 탭으로 구분된 열이 있어야 하며 머리글 행이 없어야 합니다.

   * 열 1에는 차원 요소 목록이 포함되어야 합니다.
   * 열 2에는 보고서 수신자의 이메일 주소가 포함되어야 합니다. 열 1의 지정된 요소에 대한 보고서가 열 2의 동일한 행에 있는 이메일 주소로 전송됩니다. 쉼표(공백 없음)로 구분하여 여러 이메일 주소를 입력할 수 있습니다.

      >[!NOTE]
      >
      >
      >    
      >    
      >    * 보고서를 이메일로 보내지 않는 경우, 열 2는 비워 둘 수 있지만 반드시 있어야 합니다.
      >    * 이 파일에는 빈 줄이 포함될 수 있습니다.




1. 선택 사항입니다. 보고서 이메일을 전송하려면 해당 특정 보고서 세트에 대한 파일 [!DNL Mail Report] 섹션에서 [!DNL Report.cfg] 다음을 수행해야 합니다.

   * SMTP 서버 매개 변수에 이메일을 통해 보고서를 배포하는 데 사용할 적절한 SMTP 서버를 나열합니다.
   * [수신자] 매개 변수에서 하나 이상의 이메일 주소를 나열하여 보고서를 이메일로 배포할 수 있도록 합니다. 보고서는 나열된 주소로 발송되지 않습니다. 보고서를 이메일로 전송할 수 있도록 이 매개 변수를 설정합니다. 위조 주소일 수 있지만 허용 형식(예: [!DNL jsmith@company.com])이어야 합니다.

1. 조회 파일을 보고서 세트의 폴더에 저장합니다.
1. 보고서 세트에 대한 [!DNL Report.cfg] 파일을 엽니다.
1. 차원 이름 매개 변수에 동적으로 보고서를 생성할 차원의 이름을 입력합니다.
1. 조회 파일 매개 변수에서 보고서에서 원하는 차원 요소와 수신자 이메일 주소를 포함하는 조회 파일의 위치 및 이름을 입력합니다.
1. 추가 보고서 세트에 대해 다음 단계를 반복합니다.

>[!NOTE]
>
>동적 보고서는 전체 보고서 세트가 완료될 때까지 수신자에게 이메일로 전송되지 않습니다.

## 상위 차원 요소 보고서 {#section-d8d75a6dfadd407bb18d6f32d70ebf8f}

지정된 지표별로 계산하여 상위 차원 요소에 대한 보고서를 동적으로 생성하도록 보고서 세트를 구성하려면 [!DNL Report.cfg] 파일에서 다음 매개 변수를 지정합니다.

* 차원 이름
* 상위 N 지표
* 상위 N 값
* (선택 사항) 쿼리 필터 미리 로드

이러한 매개 변수에 대한 자세한 내용은 Report.cfg [매개 변수를 참조하십시오](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

**상위 요소에 대한 동적 보고서 세트를 만들려면**

1. 보고서 세트의 [!DNL Report.cfg] 파일을 엽니다.
1. 차원 이름 매개 변수에 동적으로 보고서 세트를 생성할 차원의 이름을 입력합니다.
1. 상위 N 지표 매개 변수에서 차원을 정렬할 기준 지표 이름을 입력합니다.
1. 최상위 N 값 매개 변수에서 보고서 세트에 원하는 차원 요소의 수를 입력합니다.
1. (선택 사항) 쿼리 필터 미리 로드 매개 변수에 원하는 필터의 이름을 입력합니다.
1. 추가 보고서 세트에 대해 다음 단계를 반복합니다.
1. 보고서에서 동적 제목 시각화 사용에 대한 자세한 내용은 데이터 워크벤치 *사용 안내서를 참조하십시오*.
