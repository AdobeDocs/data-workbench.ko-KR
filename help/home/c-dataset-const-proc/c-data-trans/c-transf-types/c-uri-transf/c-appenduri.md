---
description: AppendURI 변환에서는 데이터 집합을 만드는 데 사용되는 로그 항목에서 나오는 기본값으로 정보를 추가하는 방법을 제공합니다.
title: AppendURI
uuid: 8334d4f9-2bf6-4bd0-af65-8f2b0959652d
exl-id: 0d5901c0-bd13-4499-8e26-44839aeb7413
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 1%

---

# AppendURI{#appenduri}

{{eol}}

AppendURI 변환에서는 데이터 집합을 만드는 데 사용되는 로그 항목에서 나오는 기본값으로 정보를 추가하는 방법을 제공합니다.

변환은 URI 차원을 생성하는 데 사용되는 내부 필드 끝에 이름-값 쌍을 배치합니다. 이름-값 쌍은 쿼리 문자열 키 매개 변수를 이름으로 사용하고 식별된 입력 매개 변수의 값을 쌍의 값으로 사용하여 작성됩니다. 다음 [!DNL AppendURI] 명령은 적절한 를 추가합니다. 이름-값 쌍을 [!DNL URI] 이전 [!DNL AppendURI] URI에 적용되었을 수 있는 작업입니다.

다음 [!DNL AppendURI] 변형은 에서 정의된 경우에만 작동합니다 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 이름 | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 댓글 | 선택 사항. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | 값이 URI에 추가되는 필드의 이름입니다. |  |
| 쿼리 문자열 키 | 추가할 이름-값 쌍을 만들 때 사용할 이름입니다. |  |

기존의 모델-뷰-컨트롤러 접근 방식을 사용하여 만들어진 웹 사이트를 생각해 보십시오. 이러한 시스템에서 단일 웹 페이지가 시스템에 대한 액세스 포인트가 되는 것이 일반적입니다. 이러한 사이트의 경우, 시스템에서 트래픽 패턴의 시각화는 매우 흥미롭지 않고 방문자 활용도와 트래픽 흐름에 대한 통찰력을 제공하지 않습니다. 예를 들어 다음 양식의 URI를 통해 모든 웹 요청을 단계별로 수행하는 웹 사이트를 생각해 보십시오.

* [!DNL https://www.examplesite.com/modelview.asp?id=login&name=bob]

modelview ASP 페이지는 모든 트래픽을 수신하고 쿼리의 id 필드 값을 기반으로 해당 작업을 결정합니다. 기본적으로 URI 차원은 단일 항목을 포함합니다.

* [!DNL modelview.asp]

모든 트래픽이 단일 URI를 통해 이동되고 있으므로 이를 통해 사이트를 통한 트래픽이 다소 흥미롭지 않은 매핑됩니다. 이 특정 시나리오를 해결하고 웹 사이트의 기본 아키텍처에 보다 유용한 보기를 제공하려면 [!DNL AppendURI] 는 cs-uri-query 필드에서 일부 고유한 이름-값 쌍을 시각화에 사용되는 URI 차원으로 이동하는 데 사용할 수 있습니다. 아래 표시된 변환은 이러한 변환의 세부 정보를 제공합니다.

![](assets/cfg_TransformationType_AppendURI.png)

이 예에는 시스템에서 모든 요청을 처리하는 데 사용되는 두 개의 페이지가 있습니다. [!DNL modelview.asp] 및 [!DNL xmlmodelview.asp]. 한 페이지는 브라우저 트래픽에 사용되고 다른 페이지는 시스템 간 XML 통신에 사용됩니다. 애플리케이션 서버 프로세스는 cs-uri-query의 id 이름을 사용하여 수행할 작업을 결정합니다. 따라서 ID 필드에서 값을 추출하여 URI에 추가할 수 있습니다. 그 결과, 웹 사이트를 통한 방문자 트래픽을 반영하는 다양한 범위의 URI가 수집됩니다. 여기, [!DNL String Match] 조건은 cs-uri-stem 필드에서 관심 있는 두 웹 페이지를 검색하고 다른 모든 페이지를 무시하여 변환이 적용되는 로그 항목을 결정합니다. 입력(이름-값 쌍 값)은 &quot;login&quot;인 cs-uri-query(id)의 결과입니다. 쿼리 문자열 키 매개 변수로 지정된 대로 추가되는 이름은 &quot;id&quot;입니다. 따라서 예제에서 들어오는 cs-uri 값의 경우 [!DNL URI] 차원: [!DNL /modelview.asp&id=login].
