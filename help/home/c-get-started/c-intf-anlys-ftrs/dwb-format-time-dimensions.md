---
description: 로케일에 대해 올바로 표시되도록 시간 차원을 구성합니다.
title: 시간 차원 현지화
uuid: a2098522-bf05-4680-9b78-6fb284695a0a
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# 시간 차원 현지화{#localizing-time-dimensions}

로케일에 대해 올바로 표시되도록 시간 차원을 구성합니다.

파일 내 로케일을 기반으로 시간 차원의 표시 형식을 구성할 수 있습니다(기본적으로 **[!DNL Standard Time Dimensions.cfg]** /Dataset/Transformation/Time/Standard Time Dimensions.cfg **[!DNL Server/Profiles/`<my profile>`]**&#x200B;위치).

예를 들어 북미 지역의 경우 2015년 5월 3일 날짜를 5/3/15 또는 **`%m/%d/%y`**&#x200B;로 표현할 수 있습니다. 하지만, 세계 다른 지역에서는 이 점이 값들에 대한 모호성 때문에 2015년 3월 5일로 해석될 수 `%d/%m/%y`있습니다. 이러한 상황을 방지하기 위해 관리자는 표시된 형식을 로케일의 사용자 기대에 맞게 변경할 수 있습니다.

## 1.표준 시간 Dimensions.cfg에서 기본 시간 차원 재정의 {#section-7d0b24657bef4b15abb3cbea66cb617f}

이 기능을 활성화하려면 관리자는 기존 시간 차원을 편집하거나 추가 매개 변수를 사용하여 새 시간 차원을 만들어 기본값을 무시해야 합니다.

수정된 시간 차원의 예는 다음과 같습니다.

주, **시간** , 일, 월 및 요일에 대한 형식 값은 예제의 기본값으로 설정됩니다.

>[!NOTE]
>
>이러한 줄이 생략되면 데이터 워크벤치의 동작이 변경되지 않고 기본값을 사용하여 차원이 컴파일됩니다.

```
Transformation Include = TransformationInclude:  
  Extended Dimensions = vector: 1 items 
    0 = TimeDimensions:  
      Comments = Comment: 0 items 
      Dimensions = map:  
        Day = string: Day 
        Day of Week = string: Day of Week 
        Hour = string: Hour 
        Hour of Day = string: Hour of Day 
        Month = string: Month 
        Week = string: Week 
      Hidden = bool: false 
      Input Time (1970 epoch) = string: x-unixtime 
      Week Format = string:  
  %m/%d/%y
      Hour Format = string:  
  %x %H:%M 
      Day Format = string:  
  %x
      Month Format = string:  
  %b '%y
      Hour Of Day Format = string:  
  %#H:%M
      Name = string: Visit Time 
      Parent = string: Visit 
      Week Start Day = string: Mon 
  Transformations = vector: 0 items
```

![](assets/6_4_time_format.png)

## 2.meta.cfg 파일 구성 {#section-5e077d3298dd48fda7f7bb16af9ea00c}

또한 패키지 관리자가 이러한 매개 변수와 해당 기본값을 프로필 **[!DNL meta.cfg]** 파일에 추가해야 합니다. 이를 통해 워크스테이션에서 편집할 수 있습니다.

구성된 **[!DNL meta.cfg]** 파일의 일부를 발췌했습니다.

```
dimensions = vector: 6 items 
  0 = Template: 
    ...
  ...
  5 = Template: 
    name = string: Time Dimensions 
    value = TimeDimensions: 
      Name = string:  
      Comments = Comment: 0 items 
      Hidden = bool: false 
       
  Week Format = string: %d/%m/%y 
       Hour Format = string: %x %H:%M 
       Day Format = string: %x 
       Month Format = string: %b '%y 
       Hour Of Day Format = string: %#H:%M</b> 
      Input Time (1970 epoch) = string:  
      Parent = string:  
      Week Start Day = string: Mon 
      Dimensions = map: 
        Hour of Day = string: Hour of Day 
        Day of Week = string: Day of Week 
        Hour = string: Hour 
        Day = string: Day 
        Week = string: Week 
        Month = string: Month
```

다음은 워크스테이션에 있는 **[!DNL meta.cfg]** 파일의 예입니다.

![](assets/dwb_time_format.png)

관리자는 파일 관리자로 이동하여 시간 **차원이**&#x200B;구성된 파일(예: **[!DNL Standard Time Dimensions.cfg]**&#x200B;워크스테이션)을 열고,
