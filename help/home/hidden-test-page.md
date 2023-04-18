---
title: 숨겨진 테스트 페이지
description: 이 페이지는 검색 및 목차에서 숨겨집니다
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
source-git-commit: 3c3a0289ae50d407a83ca8878af59ecde5e86e8d
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 2%

---

# 숨겨진 테스트 페이지

## 배지

배지는 컨텐츠 표시기로 사용되는 색상 레이블입니다. 예를 들어 문서를 다음으로 표시하기 위해 배지를 추가할 수 있습니다 _Beta_ 또는 섹션을 _Premium_. 배지의 색상을 변경하고 URL 및 도구 설명을 연결할 수 있습니다.

[!BADGE 배지 예]

두 가지 유형의 배지가 있으며, 각각 구문이 다릅니다.

* **메타데이터** - 페이지 상단 근처에 배지가 표시됩니다
* **인라인** - 구문이 있는 배지가 표시됩니다

### 메타데이터 배지

메타데이터에 배지 구문을 추가하면 문서의 페이지 제목(H1) 위에 배지가 추가됩니다.

배지에 이름을 지정할 수 있습니다. 예를 들어 _배지1_ 또는 _배지2_. 또는 이름이 _배지_).

메타데이터 예:

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium:** 이 예에서는 URL 및 도구 설명이 있는 Premium 배지가 표시됩니다.

* **배지:** 이 예는 시험 ID 번호가 포함된 어두운 배지를 표시합니다.

#### 인라인 배지

자체 줄이나 제목, 테이블 또는 기타 페이지 요소에 배지 정보를 지정합니다.

다음은 베타 레이블, 파란색 색상, URL 및 도구 설명이 있는 인라인 배지의 구문입니다.

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### 사용 가능한 배지 색상

배지는 Adobe 스펙트럼에 정의된 색을 사용합니다.

| 유형 | 배지 |
|---|---|
| 정보(기본값) | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| 긍정적 | [!BADGE 새로운 기능]{type=Positive url="https://www.example.com" tooltip="example.com으로 이동합니다."} |
| 부정적 | [!BADGE 중단됨]{type=negative tooltip="이 기능은 이제 수명이 종료되었습니다"} |
| 중립적 | [!BADGE 표시해야 할 수 있습니다]{type=Neutral tooltip="기수가 말에서 떨어졌다..."} |
| 주의 | [!BADGE 주의 사항]{type=Caution tooltip="노란색 상태"} |

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

* 메타데이터에는 두 개의 배지만 허용됩니다. 이 규칙은 구성이 가능하므로 예외가 필요하면 알려 주십시오.
* 배지 레이블만 필요합니다. 다음 `type`, `url`, 및 `tooltip` 매개 변수는 선택 사항입니다. 다음 `type` 매개 변수가 색상을 결정합니다. 다음 `url` 매개 변수를 사용하면 배지를 클릭하여 문서 또는 페이지를 열 수 있습니다. 다음 `tooltip` 매개 변수는 마우스오버에서 도구 설명 텍스트를 표시합니다.
* 에 배지 추가 `TOC.md` 파일에는 안내서의 모든 문서에 배지가 표시됩니다. 배지가 문서로 이동할 URL을 지정하는 경우 루트 링크(예: `/help/guide/article.md`)가 상대 링크가 아닙니다(예: `article.md`)을 클릭하여 다른 폴더의 문서를 처리합니다.
* 배지 추가 `metadata-new.md` 리포지토리의 모든 문서에 배지를 표시합니다.
* 메타데이터 배지의 경우 모든 값이 따옴표로 묶여 있는지 확인합니다. 인라인 배지의 경우 다음을 확인하십시오 `url` 및 `tooltip` 따옴표로 묶습니다.
* 유효한 유형 값은 다음과 같습니다 *정보* (기본값, 파란색), *양수* (녹색), *음수* (빨강), *중립* (진한 회색) 및 *주의* (노란색)
* 배지 레이블은 현지화됩니다.
* 여러 개의 메타데이터 배지가 지정된 경우 배지는 배지 이름(예: )을 기준으로 알파벳 순서로 표시됩니다 `badge1:` 또는 `badgeWeb`.
* 새 탭에서 URL을 열려면 다음 구문을 사용합니다.

   ```
   [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
   ```

   렌더링됨:

   [!BADGE 새 탭에서 열기]{type=Negative url="https://www.adobe.com newtab=true" tooltip="새 탭에서 adobe.com을 엽니다."}

## 텍스트 강조 표시

Workfront 팀은 예정된 기능의 미리 보기를 나타내기 위해 노란색 강조 표시를 사용할 수 있도록 요청했습니다. 작동 방법은 다음과 같습니다.

예:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

렌더링됨:

이 전체 단락은 강조 표시되지 않아야 합니다. <span class="preview"> 이 단어는 **굵게** 강조 표시된 문장 안에서</span> 그리고 이것은 단지 마지막 문장입니다.

일반적인 규칙으로, `<span class="preview">` 단락 내에서 단락 또는 텍스트를 강조 표시하려면 `<div class="preview">` 여러 단락 및 구성 요소에 대해 사용할 수 있습니다.

## 코드 블록에 대한 구문 강조 표시

Experience League은 코드 블록에 대한 구문 강조표시를 지원합니다. 다음과 같은 언어를 지정해야 합니다. `java` 구문을 올바르게 강조 표시하도록 역따옴표 세트를 연 후 유효한 언어 목록에 대해서는 [https://prismjs.com](https://prismjs.com/#supported-languages). 언어가 누락된 경우 jira 티켓을 기록하십시오.

### 코드 블록의 줄 번호 지정

추가 `{line-numbers="true"}` 언어 다음에 줄 번호를 지정할 수 있습니다.

행 번호(&amp;G;&amp;Grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**줄 번호 지정 시작**

추가 `start-number="n"` 줄 번호 구문 다음에 번호 매기기를 시작하여 1이 아닌 숫자를 시작합니다.

새 시작 줄(&amp;G;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

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

추가 `highlight="n"` 코드 블록 내의 행을 강조 표시하는 줄 번호 구문 뒤에 옵니다. 지정 `11-13, 16` 은 11부터 13까지 및 16줄을 강조 표시합니다.

선 강조 표시(&amp;G;&amp;Grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

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
