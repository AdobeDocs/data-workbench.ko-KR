---
description: 쿼리 문자열 그룹화 기능을 사용하면 많은 필드를 함께 통합할 수 있습니다.
title: 쿼리 문자열 그룹화
uuid: 7dc5ba71-984f-4899-99d2-f79b57fb616d
exl-id: 4052cf7e-abdf-4e16-9f42-521c4e719786
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---

# 쿼리 문자열 그룹화{#query-string-grouping}

{{eol}}

쿼리 문자열 그룹화 기능을 사용하면 많은 필드를 함께 통합할 수 있습니다.

쿼리 문자열 그룹화는 각 프로필에 따라 다르지만 다음 예제와 같이 변형에서 잘 작동합니다.

1. 사용자 지정 구성 파일( [!DNL E:\...\Dataset\Log Processing\SC Fields.cfg])를 클릭한 다음 변형 유형 추가 *BuildNameValuePair* 매개 변수로 사용됩니다.

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

1. 사용자 지정 구성 파일( [!DNL E:\...\Dataset\Transformation\SC Fields Transformation.cfg])를 클릭한 다음 변형 유형 추가 *ExtractNameValuePairs* 매개 변수로 사용됩니다.

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

사용자 지정 evar, prop 및 변수가 있는 필드가 많은 경우 로그 처리 중에 보고서에 필드를 결합하기 위한 이름 값 쌍을 작성할 수 있습니다. 예를 들어 명명된 값 쌍을 조합된 필드에 빌드하여 [!DNL tempDB] 파일 크기입니다.

![](assets/query_string_grouping.png)
