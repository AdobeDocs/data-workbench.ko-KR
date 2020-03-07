---
description: 토큰화 변환은 입력 문자열에 대해 정규 표현식을 반복해서 적용합니다.
solution: Analytics
title: Tokenize
topic: Data workbench
uuid: f8430e6c-ec14-4ba6-aeae-92c9f2520a63
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Tokenize{#tokenize}

토큰화 변환은 입력 문자열에 대해 정규 표현식을 반복해서 적용합니다.

그러나 [!DNL RETransform]이와 달리 [!DNL Tokenize] 전체 문자열을 일치시킬 필요는 없습니다.변환에 사용되는 정규 표현식은 입력의 하위 집합과 일치할 수 [!DNL Tokenize] 있습니다. 일치 항목을 찾은 후 [!DNL Tokenize] 마지막 일치 항목의 끝 문자부터 시작하여 정규 표현식을 다시 적용합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
|  이름  | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 대/소문자 구분 | 참 또는 거짓 대/소문자를 구분할지 여부를 지정합니다. |  |
| 설명 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없거나 정규 표현식이 입력 값과 일치하지 않는 경우에 사용할 기본값입니다. |  |
| 표현식 | 일치에 사용되는 정규 표현식. |  |
| 출력 | 출력 문자열의 이름입니다. 지정된 입력 문자열에 대해 여러 출력을 가질 수 있습니다. 출력 수는 정규 표현식의 캡처 하위 패턴 수와 일치해야 합니다. |  |

다음 예제에서는 변형이 일반 표현식을 사용하여 쿼리 문자열 이름(cs-uri-query에서)을 캡처하고 캡처된 하위 패턴(쿼리 이름)을 x-pull-query-name으로 출력합니다. [!DNL Tokenize]

![](assets/cfg_TransformationType_Tokenize.png)

쿼리 문자열 &quot;a=b&amp;c=d&quot;의 경우 출력은 &quot;a&quot; 및 &quot;c&quot;를 포함하는 벡터가 됩니다.

정규 표현식에 대한 자세한 내용은 정규 표현식을 [참조하십시오](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).
