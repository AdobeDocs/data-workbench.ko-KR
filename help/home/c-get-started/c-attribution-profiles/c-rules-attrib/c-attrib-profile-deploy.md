---
description: 속성 프로필은 상속된 즉시 사용 가능한 프로필입니다. Adobe SC 프로필 및 분석(SC/Insight) 데이터 피드와 함께 프로파일을 배포하여 디지털 채널 전반에 새로운 속성 모델을 신속하게 제공할 수 있습니다.
title: 속성 프로필 배포
uuid: acc4e92a-2af1-4993-bae7-015ece3da26c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 속성 프로필 배포{#deploying-the-attribution-profile}

속성 프로필은 상속된 즉시 사용 가능한 프로필입니다. Adobe SC 프로필 및 분석(SC/Insight) 데이터 피드와 함께 프로파일을 배포하여 디지털 채널 전반에 새로운 속성 모델을 신속하게 제공할 수 있습니다.

기본 서버에 속성 프로필을 저장한 후에는 [!DNL Profile] 디렉토리 내의 현재 프로파일에 통합하는 데 필요한 두 가지 추가 단계가 있습니다.(1) Profile.cfg 파일을 설정하고 (2) 필수 필드를 선언합니다.

## Profile.cfg 파일 설정 {#section-7531cb865d994207baba692a6fc842d7}

모든 프로파일과 마찬가지로 속성 프로필을 [!DNL profile.cfg] 파일에 추가해야 합니다. 속성 프로필은 Adobe SC 프로필에 따라 다르므로 Adobe SC 프로필은 속성 프로필 전에 구성 파일에 먼저 나열되어야 합니다.

>[!NOTE]
>
>이러한 단계는 데이터 세트를 다시 변환해야 합니다.

1. 사용자 정의 프로필 폴더에서 파일을 [!DNL profile.cfg] 엽니다. (에서 [!DNL server\Profiles\(custom profile name)\profile.cfg]열기.

1. 구성 파일에 속성 프로필이 나열되어 있지 않으면 목록에 추가합니다. ![](assets/new_profile_cfg.png)

1. 문자열이 **[!UICONTROL Attribution]** **[!UICONTROL Adobe SC]** 프로필 문자열 아래에 나열되어 있는지 확인합니다.

1. 업데이트된 [!DNL profile.cfg] 파일을 저장한 다음 프로필 관리자에서 서버에 저장합니다.

## 필수 필드 선언 {#section-23d4273af0c34b7a85ae3430e2c9350e}

속성 프로필은 사전 정의된 필드를 사용하며, 일련의 변형으로 이러한 필드를 확장 차원을 통해 새롭고 유용한 방법으로 표시합니다. 가장 즉각적인 값을 제공하기 위해 속성 프로필은 Adobe SC 프로필에서 사용할 수 있는 필드에 따라 다릅니다.

<table id="table_97751B73CCAA4B96BB162641A178A68A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 기본 변수 </th> 
   <th colname="col2" class="entry"> 필드 이름 및 디코더 위치(Adobe SC) </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 캠페인 </td> 
   <td colname="col2"> <p>x-campaign, #199 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 마케팅 채널 </td> 
   <td colname="col2"> <p>x-va_closer_detail, #162 </p> <p>x-va_instance_event, #163 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주문 이벤트 </td> 
   <td colname="col2"> <p>x-order, #206 </p> <p>x-purchaseid, #200 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 수입  </td> 
   <td colname="col2"> x-revenue, #205 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 판매량 </td> 
   <td colname="col2"> <p>x-units, #204 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 이러한 필드가 Adobe Analytics 데이터 소스를 정의하는 데 사용되는 디코더 그룹에서 선언되었는지 확인합니다. 기본 디코더 그룹이 아래에 제공됩니다 [!DNL Dataset\Log Procesing\Decoding Instructions.cfg].
1. 이러한 필드가 **[!UICONTROL Fields]** 파일 [!DNL SC Fields.cfg] 섹션에 선언되어 있는지 확인합니다. 이 파일은 아래에서 찾을 수 [!DNL Dataset\Log Processing\SC Fields.cfg]있습니다.

## 속성 추가 사항 및 문제 해결 {#section-168133a8a1a54e1281e532033878d246}

속성 프로필에서 구성 파일을 추가했습니다. 구성 파일은 [!DNL 0a_Marketing Channels.cfg]필드가 &quot;1&quot;과 일치할 때 이 [!DNL x-va_closer_detail] 필드의 값을 &quot; [!DNL x-marketing-channel][!DNL x-va_instance_event] 1&quot;이라는 새 필드에 복사합니다. 두 [!DNL x-va_closer_detail] [!DNL x-va_instant_event] 가지 모두 기본적으로 디코딩되며 버전 6.2로 업데이트할 때 사용할 수 있는 설치된 패키지의 디코딩에서 전달됩니다.

그런 다음 이 [!DNL x-marketing-channel] 필드는 마케팅 채널이라는 단순 차원에 사용됩니다.

>[!IMPORTANT]
>
>사용 중인 이전에 사용하지 않은 필드를 제거하여 프로필을 변경한 경우 [!DNL x-va_closer_detail] 및 [!DNL x-va_instance_event] 필드가 디코딩되어 사용 위해 전달되고 있는지 확인합니다.

필드가 누락된 경우 자세한 상태에 메시지가 표시됩니다.

```
<b>x-va_closer_detail</b> is not available
```

또는

```
<b>x-va_instance_event</b> is not available
```

