---
description: 로케일에 대해 올바르게 표시할 시간 차원을 구성합니다.
title: 시간 차원 현지화
uuid: a2098522-bf05-4680-9b78-6fb284695a0a
exl-id: 950fe70b-a687-4b9c-b29f-555139740809
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# 시간 차원 현지화{#localizing-time-dimensions}

{{eol}}

로케일에 대해 올바르게 표시할 시간 차원을 구성합니다.

로캘에 따라 표시된 시간 차원 형식을 구성할 수 있습니다 **[!DNL Standard Time Dimensions.cfg]** 파일(기본적으로 다음 위치에 있음) **[!DNL Server/Profiles/`<my profile>`/Dataset/Transformation/Time/Standard Time Dimension.cfg]**).

예를 들어, 북아메리카에서는 2015년 5월 3일 날짜를 5/3/15으로 표현할 수 있습니다. **`%m/%d/%y`**. 하지만, 세계의 다른 지역에서는, 이것은 `%d/%m/%y`값의 모호성 때문에 2015년 3월 5일 이러한 상황을 방지하기 위해 관리자는 로케일의 사용자 기대에 맞게 표시된 형식을 변경할 수 있습니다.

## 1. Standard Time Dimension.cfg에서 기본 시간 Dimension 무시 {#section-7d0b24657bef4b15abb3cbea66cb617f}

이 기능을 사용하려면 관리자가 기존 시간 차원을 편집하거나 추가 매개 변수로 새 시간 차원을 생성하여 기본값을 무시해야 합니다.

수정된 시간 차원의 예는 다음과 같습니다.

다음 **형식** 주, 시간, 일, 월 및 시간 값이 예제의 기본값으로 설정됩니다.

>[!NOTE]
>
>이러한 라인을 생략하면 Data Workbench의 동작이 변경되지 않고 기본값을 사용하여 차원을 컴파일합니다.

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

## 2. meta.cfg 파일을 구성합니다 {#section-5e077d3298dd48fda7f7bb16af9ea00c}

또한 패키지 관리자가 이러한 매개 변수와 해당 기본값을 프로필의 **[!DNL meta.cfg]** 파일. 이를 통해 워크스테이션에서 편집할 수 있습니다.

다음은 구성된 **[!DNL meta.cfg]** 파일.

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

다음은 의 예입니다 **[!DNL meta.cfg]** 워크스테이션의 파일:

![](assets/dwb_time_format.png)

그런 다음 관리자는 **파일 관리자**&#x200B;를 눌러 시간 차원이 구성된 파일(예: **[!DNL Standard Time Dimensions.cfg]**)을 편집하거나 워크스테이션에서 를 사용하여 편집할 수 있습니다.
