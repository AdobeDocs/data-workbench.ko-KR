---
description: 쿼리 문자열 그룹화를 사용하면 많은 수의 필드를 통합할 수 있습니다.
title: 쿼리 문자열 그룹화
uuid: 7dc5ba71-984f-4899-99d2-f79b57fb616d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 쿼리 문자열 그룹화{#query-string-grouping}

쿼리 문자열 그룹화를 사용하면 많은 수의 필드를 통합할 수 있습니다.

쿼리 문자열 그룹화는 각 프로필에 고유하지만 다음 예와 같이 변형에서 잘 작동합니다.

1. 사용자 지정 구성 파일()을 추가한 다음 변환 유형 BuildNameValuePair를 [!DNL E:\...\Dataset\Log Processing\SC Fields.cfg]매개 변수로 추가하여 번들할 ** 쌍을 만듭니다.

   ```
   2 = BuildNameValuePair:  
         Comments = Comment: 0 items 
         Condition = AndCondition: 0 items 
         Delimiter = string:  
         Input Columns = vector: 1 items 
           0 = Column:  
             Column Name = string: e100 
             Field Name = string: x-cust100 
             ...  
     (all the fields you wish to build)
             Name = string: Custom Events 
             Output = string: x-event-list       
   ```

1. 사용자 지정 구성 파일()을 추가한 다음 변형 유형 ExtractNameValuePairs를 매개 변수로 추가하여 압축된 데이터를 사용하려는 필드에 추출하기 위한 [!DNL E:\...\Dataset\Transformation\SC Fields Transformation.cfg]새 ** 파일을 만듭니다.

   ```
   2 = ExtractNameValuePairs:  
         Comments = Comment: 0 items 
         Condition = AndCondition: 0 items 
         Delimiter = string:  
         Input Field = string: x-event-list 
         Name = string: Custom Events 
         Output Columns = vector: 1 items 
           0 = Column:  
             Column Name = string: e100 
             Field Name = string: x-cust100 
             ...  
     (all the fields you wish to extract) 
             Name = string: Custom Events 
             Output = string: x-event-list   
   ```

## 기타 사용 {#section-cc5d2b0c9e194fc88a5a18a06ef22f5e}

사용자 지정 evar, prop 및 변수가 있는 필드가 많이 있는 경우 로그 처리 중에 이름 값 쌍을 작성하여 보고서에 필드를 결합할 수 있습니다. 예를 들어 명명된 값 쌍을 결합된 필드로 만들어 [!DNL tempDB] 파일 크기를 줄일 수 있습니다.

![](assets/query_string_grouping.png)
