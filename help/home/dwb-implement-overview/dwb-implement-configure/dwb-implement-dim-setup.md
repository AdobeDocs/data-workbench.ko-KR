---
description: 이 섹션에서는 다양한 유형의 Dimension과 DWB에서 설정하는 방법을 설명합니다.
title: 차원 설정
uuid: 5b40cb43-7790-4b87-a0bb-be395a420157
exl-id: 04afd773-e938-49f7-83c9-1d706a6dc525
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 4%

---

# 차원 설정{#dimension-setup}

{{eol}}

이 섹션에서는 다양한 유형의 Dimension과 DWB에서 설정하는 방법을 설명합니다.

## Dimension 소개 {#section-dac631943df24706827cedc6f0641543}

가장 기본적인 수준에서 차원은 데이터 집합에 있는 데이터를 분류할 수 있는 카테고리입니다.

우수 사례: 데이터 스키마의 Dimension은 모든 이름을 제공할 수 있습니다. 이 과정에서 사용 및 설명한 Dimension 이름은 가장 좋은 것으로 간주됩니다. Dimension 이름은 다르게 지정할 수 있습니다. 다른 데이터 세트에 노출되면 데이터 세트에 차이점이 표시됩니다. 차원의 이름이 아닌 목적을 이해하는 것이 중요합니다. 예를 들어 &quot;방문자&quot;, &quot;고객&quot;, &quot;사람&quot;, &quot;소비자&quot; 또는 &quot;사용자&quot;라고 하든, 이러한 용어가 단일 사용자에 대한 정보를 수집하는 데 사용되는 가장 높은 수준 계산 가능한 차원을 참조하는 데 일반적으로 사용되는 용어임을 이해하는 것이 중요합니다.

자세한 내용은 [데이터 집합 구성](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/c-dataset-constr.html) 안내서.

## DWB의 Dimension 유형 {#section-a4fbb7bf2bde44528ac0f94a96465862}

Data Workbench에는 두 가지 유형의 차원이 있습니다. 확장 Dimension 및 파생 Dimension.

확장된 Dimension은 &quot;원시&quot; 데이터 파일의 필드에서 만들어집니다. 확장 차원은 &quot;원시&quot; 데이터를 분류하고 데이터 간에 존재하는 관계를 지정하는 데 사용됩니다. 확장된 차원은 Data Workbench 설계자에 의해 생성됩니다.

파생된 Dimension은 기존 확장 차원 정의를 사용하여 데이터 세트를 처리한 후 &quot;클라이언트 측에서&quot; 사용자가 만듭니다. 예를 들어, 기존 URI 차원을 기반으로 사용자는 지정된 URI 대신 사용자에게 더 친숙한 페이지 이름을 표시하는 파생된 페이지 이름 차원을 생성하도록 선택할 수 있습니다. 모든 차원은 차원을 구성하기 위해 함께 분류(그룹화된)된 요소 또는 항목으로 구성됩니다. 아래는 3개의 차원과 해당 요소입니다.

파생된 측정기준 중에는 다양한 시각화 유형을 파생시키기 위해 자동으로 생성되는 것이 많습니다. 예를 들어 사용자가 사이트 또는 프로세스 맵을 빌드하면 DWB 서버에서 접두사 차원을 만듭니다. 보고 시간 측정기준 등의 기타 측정기준은 프로필의 Dimensions 디렉토리에 있는 파일로 정의됩니다.

>[!NOTE]
>
>주어진 차원에 나타나는 요소는 데이터 집합에 로드되도록 선택한 레코드에 있는 값만 반영합니다. 예를 들어 &quot;5월 12일&quot;에 대한 데이터가 없으면 해당 달이 &#39;월&#39; 차원에 나타나지 않습니다.

## 확장된 차원 {#section-5fc51fa539034941a30a2df606f7d727}

확장 차원 유형

**1) 가산 Dimension**

가장 높은 수준에서 가산 차원입니다. 가산 차원은 두 가지 주요 기능을 제공합니다. 먼저 계산하려는 요소의 차원입니다. 다시 말해, 카운터 테이블은 다음과 같은 질문에 대답합니다.

* 홈 페이지를 방문한 방문자는 몇 명입니까?
* google.com에서 몇 번이나 방문했습니까?

이러한 이유로, countables는 종종 지표를 만드는 기본 빌딩 블록으로 사용됩니다.

counttable의 두 번째 주요 기능은 데이터 집합 스키마 구조의 중추를 구성하는 것입니다. 데이터 스키마와 기타 모든 차원은 아래에 그룹화되고 계산 가능한 차원에 속하도록 구성되어 있습니다. 다시 말해, 차원을 &quot;카테고리&quot;로 간주하면 카운테이블이 이러한 &quot;카테고리&quot;를 그룹으로 구성하는 방법입니다.

차원을 가산 차원 아래에 그룹화할 때 가산 차원의 &quot;수준&quot;에 있다고 합니다. 예를 들어 &#39;이메일 주소&#39;는 방문자 수준에 있을 수 있고 &quot;브라우저&quot;는 방문 수준에 있습니다. &quot;상위&quot; 및 &quot;하위&quot;는 계산 가능한 차원과 그 아래에 그룹화된 차원 간의 관계를 의미합니다. 예를 들어 방문자는 이메일 주소의 &quot;상위&quot;입니다. 반대로 이메일 주소는 방문자의 &quot;하위&quot;입니다.

**2) 단순 Dimension**

모든 차원의 가장 일반적인 차원은 단순 차원입니다. 단순 차원은 상위 가산 차원과 일대다 관계를 가지며 해당 요소를 볼 수 있도록 시각화에 일반적으로 사용됩니다. 즉, 가산 차원은 단순 차원에 대해 하나의 값을 가질 수 있지만 단순 차원은 하나 이상의 가산 테이블에 속할 수 있습니다. 예를 들어 고객의 이름은 &#39;John&#39;이지만 고객은 이름을 하나만 가질 수 있지만 다른 많은 고객은 &#39;John;&#39;이라는 이름을 사용할 수 있습니다. 다른 예로, 웹 사이트에 대한 특정 방문에는 하나의 브라우저(예: Firefox)만 사용할 수 있지만 해당 브라우저는 여러 다른 방문에 사용할 수 있습니다.

가산 차원이 &quot;몇 개?&quot;에 응답하면 단순 차원이 &quot;어느 차원?&quot;에 답합니다. 가산 차원 섹션에서 사용되는 것과 동일한 예제 사용 페이지 이름은 단순 차원입니다. 테이블과 단순 차원, 페이지 이름을 사용하여 다음과 같은 질문에 답변할 수 있습니다.

* &quot;페이지 보기 수가 가장 많은 페이지는 무엇입니까?&quot;
* &quot;모든 장바구니 페이지 중 가장 많은 방문 횟수를 기록한 페이지는 무엇입니까?&quot;

**3) 다대다 Dimension**

다대다 차원은 상위 가산 차원과 다대다 관계를 갖습니다. 예를 들어 외부 검색어라는 차원이 방문 수준에 있는 경우, 주어진 외부 검색어는 하나 이상의 방문에서 사용할 수 있으며 주어진 방문에는 하나 이상의 외부 검색어가 포함될 수 있습니다. 따라서 외부 검색어는 다대다 차원입니다.

**4) 숫자 Dimension**

숫자 차원은 숫자 값을 갖는 단순 차원의 유형입니다. 숫자 차원이 지표에 사용하기 위해 만들어지는 경우가 많습니다. 숫자 차원의 예로는 &#39;수입&#39;, &#39;주문&#39; 및 &#39;판매량&#39;이 있습니다. 위의 예에서 &#39;고객 주문&#39;은 숫자 차원입니다.
**5) 비정상 Dimension** 비정상 차원은 상위 가산 차원과 일대일 관계가 있는 차원입니다. 비정상 차원은 ID 데이터와 같은 높은 카디널리티(많은 고유 요소)를 갖는 차원에 사용되는 경우가 많습니다. 예를 들어 방문자는 하나의 사용자 ID만 가질 수 있으며 사용자 ID는 하나의 방문자에만 속할 수 있습니다. 따라서, 이것은 일대일 관계이며 비정상 차원일 수 있습니다.

예를 들어 Geometrixx 웹 사용자 ID는 고객 수준에서 비정상 차원입니다. 비정상 항목이므로 상위 차원과 일대일 관계가 있습니다. 즉, 각 웹 사용자 ID에는 고객이 하나씩 있고 각 고객에는 웹 사용자 ID가 하나만 있습니다. 따라서, &#39;고객&#39; 지표는 Geometrixx 웹 사용자 ID의 각 요소에 대해서만 &#39;1&#39;일 수 있습니다.

**6) 시간 Dimension**

시간 차원을 사용하면 지정된 타임스탬프 필드를 기반으로 주기적 또는 절대 로컬 시간 차원 집합을 만들 수 있습니다. 시간 차원의 예로는 &#39;일&#39;, &#39;시간&#39;, &#39;주&#39; 및 &#39;시간&#39;이 있습니다. 위의 예에서 &#39;시간&#39; 테이블은 다른 시간 동안 받은 방문 및 페이지 보기 수를 보여줍니다.

>[!NOTE]
>
>표시 형식에 사용되는 % 이스케이프가 표준 C 라이브러리와 동일합니다 *strftime*.

## 확장 차원 정의 {#section-38ee124ec74b43fb95f13194a9582b97}

확장 Dimension 정의 단계:

1. 데이터 세트 프로필에서 작업하는 동안 프로필 관리자를 열고 데이터 세트 를 클릭하여 해당 콘텐츠를 표시합니다.
1. 확장 차원을 정의하려는 Transformation.cfg 파일 또는 Transformation Dataset Include 파일을 엽니다.
1. 변형 을 마우스 오른쪽 단추로 클릭하고 새로 추가 > `<Extended dimension type>`.
1. 확장 차원에 대한 적절한 정보를 입력합니다. 변형 유형에 대한 설명 및 해당 매개 변수에 대한 정보는 다음 섹션을 참조하십시오.

   * [가산 차원](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-count-dim.html)
   * [단순 차원](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-simple-dim.html)
   * [다대다 차원](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-many-dim.html)
   * [숫자 차원](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-num-dim.html)
   * [비정상 차원](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-denormal-dim.html)
   * [시간 차원](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/extended-dimensions/extended-dimensions-types/c-time-dim.html)

1. 정의한 확장 차원에 대해 설명 매개 변수에 하나 이상의 주석 라인을 추가하여 차원을 추가로 설명하거나 해당 용도에 대한 메모를 추가할 수 있습니다. 주석을 추가하려면 *댓글* 레이블을 지정하고* 새로 추가 > 주석 줄*을 클릭합니다.

1. 구성 파일에서 확장 차원을 정의한 후 파일을 로컬로 저장하고 DWB 서버의 데이터 세트 프로필에 저장합니다.

## 확장 차원 숨기기 {#section-02339fb51658418eabc10186cd5957d7}

확장 Dimension은 DWB의 Dimension 메뉴에 표시되지 않도록 숨길 수 있습니다. 차원을 숨기려면 차원 정의에서 숨김 속성을 &quot;True&quot;로 설정합니다.
