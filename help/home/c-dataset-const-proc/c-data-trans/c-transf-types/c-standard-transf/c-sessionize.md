---
description: 웹 사이트 트래픽에서 수집된 데이터로 작업하는 경우 세션 크기 변환을 사용하여 세션이 정의된 방식을 결정할 수 있습니다.
title: 세션
uuid: c6e2487a-80e5-4e00-b4d4-2ce013fac3ea
exl-id: bb25cb4b-7185-4524-8ff5-740b672e1cd9
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 1%

---

# 세션{#sessionize}

웹 사이트 트래픽에서 수집된 데이터로 작업하는 경우 세션 크기 변환을 사용하여 세션이 정의된 방식을 결정할 수 있습니다.

변형은 타임스탬프 및 추적 ID를 입력하여 사용되며 각 로그 항목의 세션 번호를 출력합니다. 세션 번호는 지정된 추적 ID가 있는 첫 번째 세션에 대해 &quot;1&quot;이고, 추적 ID가 동일한 두 번째 세션에 대해 &quot;2&quot;입니다. 출력물은 각 세션에 대한 고유 값이 있기 때문에 세션 키로 직접 사용할 수 있습니다.

>[!NOTE]
>
>이 작업을 수행하려면 [!DNL Sessionize] 변형이 소스 데이터의 추적 ID로 지정된 시간에 데이터를 정렬하고 그룹화해야 합니다. 따라서 [!DNL Sessionize]은 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일에 정의된 경우에만 작동합니다.

<table id="table_34984DF9340149C0A5016F08EABAD158"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 변환의 설명형 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 변형에 대한 참고 사항 </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 타임스탬프 </td> 
   <td colname="col2"> 사용할 타임스탬프 값이 들어 있는 필드입니다. </td> 
   <td colname="col3"> x-timestamp </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 추적 ID </td> 
   <td colname="col2"> <p>사용할 추적 ID 값이 포함된 필드입니다. 값은 64비트(16자리) 또는 16자리 이하의 16진수 또는 16자리 이하의 십진수 정수여야 합니다. </p> <p> <p>참고:추적 ID에 x-trackingid 이외의 필드를 사용하려면 먼저 필드를 해시 처리해야 합니다. <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-hash.md#concept-9c353923264941c3aea4428fed66d369"> 해시</a>을 참조하십시오. </p> </p> </td> 
   <td colname="col3"> x-trackingid </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>최대 세션 기간 </p> </td> 
   <td colname="col2">새 세션을 시작하기 전의 세션 길이입니다. 이렇게 하면 자동 컨텐츠가 있는 웹 페이지가 임의로 긴 세션을 만들 수 없게 됩니다. <span class="wintitle"> 시간 초과 조건</span>이 충족되고 클릭 레퍼러가 내부 도메인 매개 변수의 항목 중 하나로 설정된 경우 최대 세션 지속 시간을 사용하여 세션의 끝을 정의합니다. 어떤 세션은 클릭이 포함되는지에 관계없이 지정된 최대 세션 지속 시간보다 길지 않을 수 있습니다. 권장 값은 48시간입니다. 최대 세션 기간 및 내부 도메인 매개 변수에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519"> 웹 데이터의 구성 설정</a>을 참조하십시오. </td> 
   <td colname="col3"> 48시간 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 세션 번호 </td> 
   <td colname="col2"> 세션 번호가 저장되는 필드입니다. 이 필드에는 각 방문자에 대한 각 세션에 대한 고유한 값이 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 시간 초과 </td> 
   <td colname="col2"> <p>한 세션의 끝과 새 세션의 시작(사용자 세션을 정의하는 데 사용되는 일반적인 시간 초과)을 결정하기 위해 지정된 방문자의 로그 항목 사이에 전달해야 하는 시간입니다. 이 매개 변수의 권장 값은 30분입니다. 시간 초과 조건이 충족되지 않고 클릭 레퍼러가 내부 도메인 매개 변수의 레퍼러 중 하나로 설정되지 않은 경우 세션 시간 초과를 사용하여 세션을 정의합니다. </p> <p> 시간 초과 조건이 충족되고 로그 항목의 cs(referrer-domain)가 내부 도메인 목록에 있는 경우 최대 세션 지속 시간은 현재 로그 항목이 기존 세션의 일부인지 새 세션의 시작인지를 결정합니다. </p> <p> 세션 시간 초과 매개 변수에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519"> 웹 데이터의 구성 설정</a>을 참조하십시오. </p> </td> 
   <td colname="col3"> 30분 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 초과 조건 </td> 
   <td colname="col2"> 로그 항목이 새 세션의 시작으로 간주되려면 충족해야 하는 조건입니다. 로그 항목과 이전 로그 항목 간에 전달되는 시간은 세션 시간 초과 매개 변수의 값 이상이어야 합니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

다음 상황 중 하나가 발생하면 새 세션이 시작됩니다.

* 추적 ID가 변경됩니다.
* 마지막 로그 항목 이후의 시간은 세션 시간 초과 매개 변수의 값과 같으며 시간 초과 조건이 충족됩니다.
* 마지막 세션의 첫 번째 로그 항목이 최대 세션 기간 매개 변수의 값을 초과하는 시간입니다.

>[!NOTE]
>
>[!DNL Session Parameters.cfg] 파일에 매개 변수로 최대 세션 지속 시간 및 세션 시간 초과를 이미 정의한 경우에는 구성에 해당 세션 값을 입력하지 마십시오. 다음 예제와 같이 *$(매개 변수 이름)*&#x200B;을 입력하여 매개 변수를 참조할 수 있습니다. 이러한 매개 변수에 대한 자세한 내용은 [웹 데이터의 구성 설정](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)을 참조하십시오.

이 예의 [!DNL Sessionize] 변환은 x-timestamp 및 x-trackingid 필드를 입력하고 x-session-key 필드에 각 로그 항목의 세션 번호를 기록합니다. 변환의 [!DNL Timeout Condition]은(는) [!DNL Neither] 조건을 기반으로 합니다.로그 항목의 cs(referrer-domain) 필드가 내부 도메인 매개 변수의 멤버와 일치하면 조건이 false로 평가됩니다. 내부 도메인 및 세션 시간 초과 매개 변수에 대한 참조를 확인하십시오.

[!DNL NeitherCondition]에 대한 자세한 내용은 [조건](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md)을 참조하십시오. 내부 도메인 및 세션 시간 초과 매개 변수에 대한 자세한 내용은 [웹 데이터의 구성 설정](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)을 참조하십시오.

![](assets/cfg_TransformationType_Sessionize.png)
