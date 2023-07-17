---
title: 숨겨진 테스트 페이지
description: 이 페이지는 검색 및 목차에서 숨겨집니다.
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Premium 다운로드"
badgeExam: label="시험 ADO-E903" type="neutral"
exl-id: 25669153-b90c-4cf6-81aa-cabcbf2cbcb6
source-git-commit: 3480cc9b82a5561a364a88f3d09c14cca56a0c7a
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 4%

---

# 숨겨진 테스트 페이지

## 문제 미리보기

다음 단락이 VSC 미리 보기에서 제대로 렌더링되지 않습니다. 이유를 잘 모르겠어요.

암호를에서 관리하는 경우 [!DNL Adobe], 다음을 수행할 수 있습니다. [Adobe 계정의 암호 변경](https://helpx.adobe.com/manage-account/using/change-or-reset-password.html){target="_blank"}.

## 메모 유형

지원되는 모든 메모 유형입니다.

>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard tip.

>[!IMPORTANT]
>
>중요한 메모입니다.

>[!WARNING]
>
>이것은 경고입니다.

>[!CAUTION]
>
>이것은 주의사항입니다.

>[!ADMIN]
>
>관리로 렌더링되는 관리 노트입니다. EXL만 해당.

>[!AVAILABILITY]
>
>가용성 정보입니다. EXL만 해당.

>[!PREREQUISITES]
>
>사전 요구 사항 참고입니다. EXL만 해당.

>[!INFO]
>
>정보 노트입니다. EXL만 해당.

>[!ERROR]
>
>오류 노트입니다. EXL만 해당.

>[!SUCCESS]
>
>성공 노트입니다. EXL만 해당.

>[!MORELIKETHIS]
>
>* 페이지 1
>* 페이지 2

## 배지

배지는 콘텐츠 표시기로 사용되는 색상 레이블입니다. 예를 들어 배지를 추가하여 문서를 로 표시할 수 있습니다. _베타_ 또는 섹션을 다음으로 표시 _Premium_. 배지의 색상을 변경하고 URL 및 도구 설명을 연결할 수 있습니다.

[!BADGE 배지 예]

배지에는 각각 다른 구문을 가진 두 가지 유형이 있습니다.

* **메타데이터** - 페이지 상단 근처에 배지를 표시합니다.
* **인라인** - 구문이 있는 배지를 표시합니다.

### 메타데이터 배지

메타데이터에 배지 구문을 추가하면 문서의 페이지 제목(H1) 위에 배지가 배치됩니다.

예를 들어 배지의 이름을 지정할 수 있습니다. _배지1_ 또는 _배지2_. 또는 이름이 로 시작하는 한 보다 창의적일 수 있습니다 _배지_).

메타데이터 예:

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **배지 프리미엄:** 이 예에서는 URL 및 도구 설명이 있는 Premium 배지가 표시됩니다.

* **배지 테스트:** 이 예에서는 시험 ID 번호가 포함된 어두운 배지가 표시됩니다.

#### 인라인 배지

해당 줄 또는 제목, 테이블 또는 기타 페이지 요소에 배지 정보를 지정합니다.

베타 레이블, 파란색, URL 및 도구 설명이 있는 인라인 배지의 구문은 다음과 같습니다.

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### 사용 가능한 배지 색상

배지는 Adobe 스펙트럼에 정의된 색상을 사용합니다.

| 유형 | 배지 |
|---|---|
| 정보(기본값) | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| 긍정적 | [!BADGE 새로운 기능]{type=Positive url="https://www.example.com" tooltip="example.com으로 이동"} |
| 부정적 | [!BADGE 중단됨]{type=negative tooltip="이 기능은 현재 사용 중단되었습니다."} |
| 중립적 | [!BADGE 표시해야 할 수 있습니다]{type=Neutral tooltip="기수가 말에서 떨어졌다..."} |
| 주의 | [!BADGE 주의]{type=Caution tooltip="노란색 상태"} |

구문 예

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### 배지 요구 사항

* 메타데이터에는 배지가 두 개만 허용됩니다. 이 규칙은 구성 가능하므로 예외가 필요한 경우 알려주십시오.
* 배지 레이블만 필요합니다. 다음 `type`, `url`, 및 `tooltip` 매개 변수는 선택 사항입니다. 다음 `type` 매개 변수가 색상을 결정합니다. 다음 `url` 매개 변수를 사용하면 사용자가 배지를 클릭하여 문서 또는 페이지를 열 수 있습니다. 다음 `tooltip` 매개 변수는 마우스오버에 도구 설명 텍스트를 표시합니다.
* 에 배지 추가 `TOC.md` 파일에는 안내서의 모든 문서에 대한 배지가 표시됩니다. 배지가 문서로 이동할 때 사용할 URL을 지정하는 경우 루트 링크를 사용해야 합니다(예: `/help/guide/article.md`) 상대 링크가 아닙니다(예: `article.md`)를 사용하여 다른 폴더의 문서를 관리할 수 있습니다.
* 배지 추가 `metadata-new.md` 보고서의 모든 문서에 배지를 표시합니다.
* 메타데이터 배지의 경우 모든 값이 따옴표로 묶여 있는지 확인합니다. 인라인 배지의 경우 다음을 확인하십시오 `url` 및 `tooltip` 따옴표로 묶여 있습니다.
* 유효한 유형 값은 다음과 같습니다. *정보* (기본값, 파란색), *양수* (녹색), *부정적* (빨간색), *중립* (진한 회색) 및 *주의* (노란색).
* 배지 레이블은 현지화됩니다.
* 여러 메타데이터 배지를 지정한 경우 배지는 다음과 같이 배지 이름을 기반으로 알파벳 순서로 표시됩니다. `badge1:` 또는 `badgeWeb`.
* URL을 새 탭에서 열려면 다음 구문을 사용합니다.

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  렌더링됨:

  [!BADGE 새 탭에서 열기]{type=Negative url="https://www.adobe.com newtab=true" tooltip="새 탭에서 adobe.com 열기"}

## 텍스트 강조 표시

Workfront 팀이 예정된 기능의 미리 보기를 표시하기 위해 노란색 강조 표시를 사용할 수 있도록 요청했습니다. 작동 방식은 다음과 같습니다.

예제 1:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

렌더링됨:

이 전체 단락은 강조 표시되지 않아야 합니다. <span class="preview"> 이 단어는 **굵게** 강조 표시된 문장 내부.</span> 그리고 이것은 단지 마지막 문장입니다.

예제 2:

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/home/assets/analytics-icon-24.png)

Last highlighted item.

</div>

Not highlighted
```

렌더링됨:

강조 표시는 이 단락 다음에 시작해야 합니다.

<div class="preview">

DIV 시작

새 단락과 이미지입니다.

![이미지](/help/home/assets/analytics-icon-24.png)

마지막으로 강조 표시된 항목.

</div>

강조 표시되지 않음

## 코드 블록에 대한 구문 강조 표시

Experience League은 코드 블록에 대한 구문 강조 표시를 지원합니다. 다음과 같은 언어를 지정해야 합니다. `java` 열기 백 틱 후에는 구문이 제대로 강조 표시되었는지 확인합니다. 유효한 언어 목록은 다음을 참조하십시오. [https://prismjs.com](https://prismjs.com/#supported-languages). 누락된 언어가 있으면 jira 티켓을 기록하십시오.

### 코드 블록의 행 번호 매기기

추가 `{line-numbers="true"}` 줄 번호를 사용하려면 언어 뒤에 추가하십시오.

줄 번호(&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**줄 _에서 번호 매기기 시작**

추가 `start-number="n"` 줄 번호 구문 뒤에 숫자를 붙여서 1이 아닌 다른 숫자에서 번호 매기기를 시작합니다.

새 시작 라인(&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### 코드 블록의 선 강조 표시

추가 `highlight="n"` 코드 블록 내의 행을 강조 표시하는 행 번호 구문 뒤에. 지정 중 `11-13, 16` 에서는 11행부터 13행까지 및 16행을 강조 표시합니다.

선 강조 표시(&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```
