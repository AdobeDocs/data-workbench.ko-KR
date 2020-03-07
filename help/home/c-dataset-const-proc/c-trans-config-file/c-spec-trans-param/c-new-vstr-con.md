---
description: 새 방문자 조건은 웹 사이트 데이터와 함께 어떤 방문자가 데이터 세트에 포함할 것으로 간주되는지 확인하는 조건 작업입니다.
solution: Analytics
title: 새 방문자 조건
topic: Data workbench
uuid: e9733109-5bf3-47ce-974c-d68264291f19
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 새 방문자 조건{#new-visitor-condition}

새 방문자 조건은 웹 사이트 데이터와 함께 어떤 방문자가 데이터 세트에 포함할 것으로 간주되는지 확인하는 조건 작업입니다.

The [!DNL New Visitor Condition] defines the first log entry (order by time) for a visitor that to be used in the dataset, and all subsequent log entries are includes in the dataset whether they meet this condition. 방문자와 시간별로 데이터를 [!DNL New Visitor Condition] 정렬해야 하므로 데이터 세트 생성의 변환 단계 동안에만 적용됩니다.

이 예제에 [!DNL New Visitor Condition] 표시된 대로 이메일 캠페인에 응답하는 방문자에 대한 로그 항목만 포함하는 데이터 세트를 만듭니다. 이 작업은 [!DNL NotEmptyCondition] 테스트(비어 있지 [않음](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-1decb9d887894073a1b6b3d985729ac8)참조)와 [!DNL x-campaign-email] 필드를 정규 표현식에 대한 입력으로 사용하여 수행됩니다. 조건을 충족하는 새 방문자가 식별되면 해당 방문자에 대한 모든 로그 항목이 캡처됩니다.

![](assets/cfg_Transformation_NewVisitorCondition.png)

