---
description: 속성 프로필은 상속된 바로 가기 프로필입니다. Adobe SC 프로필 및 Analytics(SC/Insight) 데이터 피드와 함께 프로필을 배포하여 디지털 채널 간에 새로운 속성 모델을 빠르게 표시할 수 있습니다.
title: 속성 프로필 배포
uuid: acc4e92a-2af1-4993-bae7-015ece3da26c
exl-id: 287e1710-7e74-4904-b258-7b811ad484b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 3%

---

# 속성 프로필 배포{#deploying-the-attribution-profile}

{{eol}}

속성 프로필은 상속된 바로 가기 프로필입니다. Adobe SC 프로필 및 Analytics(SC/Insight) 데이터 피드와 함께 프로필을 배포하여 디지털 채널 간에 새로운 속성 모델을 빠르게 표시할 수 있습니다.

기본 서버에 속성 프로필을 저장한 후에서 현재 프로필에 통합하는 데 필요한 두 가지 추가 단계가 있습니다 [!DNL Profile] 디렉토리: (1) Profile.cfg 파일을 설정하고 (2) 필수 필드를 선언합니다.

## Profile.cfg 파일 설정 {#section-7531cb865d994207baba692a6fc842d7}

모든 프로필과 마찬가지로 속성 프로필을 [!DNL profile.cfg] 파일. 속성 프로필은 Adobe SC 프로필에 따라 다르므로 Adobe SC 프로필은 속성 프로필 전에 구성 파일에 먼저 나열되어야 합니다.

>[!NOTE]
>
>이러한 단계에는 데이터 세트를 다시 변환해야 합니다.

1. 를 엽니다. [!DNL profile.cfg] 파일을 사용자 지정 프로필 폴더에 넣습니다. (여는 위치) [!DNL server\Profiles\(custom profile name)\profile.cfg].

1. 구성 파일에 속성 프로필이 나열되지 않으면 목록에 추가합니다. ![](assets/new_profile_cfg.png)

1. 다음을 확인합니다. **[!UICONTROL Attribution]** 문자열은 아래에 나열됩니다 **[!UICONTROL Adobe SC]** 프로필 문자열.

1. 업데이트된 내용을 저장합니다 [!DNL profile.cfg] 파일을 만든 다음 프로필 관리자에서 서버에 저장합니다.

## 필수 필드 선언 {#section-23d4273af0c34b7a85ae3430e2c9350e}

속성 프로필은 사전 정의된 필드를 사용하고 일련의 변형을 사용하면 확장 차원을 통해 이러한 필드를 새롭고 유용한 방식으로 노출합니다. 가장 즉각적인 값을 제공하기 위해 속성 프로필은 Adobe SC 프로필에서 사용할 수 있는 필드에 따라 다릅니다.

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
   <td colname="col1"> 매출 </td> 
   <td colname="col2"> x-revenue, #205 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 판매량 </td> 
   <td colname="col2"> <p>x-units, #204 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 이러한 필드가 Adobe Analytics 데이터 소스를 정의하는 데 사용되는 디코더 그룹에서 선언되었는지 확인합니다. 기본 디코더 그룹은 아래에 제공됩니다 [!DNL Dataset\Log Procesing\Decoding Instructions.cfg].
1. 이러한 필드가 **[!UICONTROL Fields]** 섹션 [!DNL SC Fields.cfg] 파일. 이 파일은 아래에 있습니다 [!DNL Dataset\Log Processing\SC Fields.cfg].

## 속성 추가 및 문제 해결 {#section-168133a8a1a54e1281e532033878d246}

속성 프로필에 구성 파일, [!DNL 0a_Marketing Channels.cfg]- 의 값을 복사합니다. [!DNL x-va_closer_detail] 새 필드에 [!DNL x-marketing-channel], 다음의 경우 [!DNL x-va_instance_event] 필드가 &quot;1&quot;과 일치합니다. 둘 다 [!DNL x-va_closer_detail] 및 [!DNL x-va_instant_event] 는 기본적으로 디코딩되고 버전 6.2로 업데이트할 때 사용할 수 있는 설치된 패키지의 디코딩에서 전달됩니다.

다음 [!DNL x-marketing-channel] 그런 다음 마케팅 채널이라는 단순 차원에 필드가 사용됩니다.

>[!IMPORTANT]
>
>현재 사용 중인 이전에 사용하지 않은 필드를 제거하여 프로필을 수정한 경우 [!DNL x-va_closer_detail] 및 [!DNL x-va_instance_event] 필드를 디코딩하여 사용 중입니다.

필드가 누락되면 세부 상태의 메시지가 표시됩니다.

```
<b>x-va_closer_detail</b> is not available
```

또는

```
<b>x-va_instance_event</b> is not available
```
