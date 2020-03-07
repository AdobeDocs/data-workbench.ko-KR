---
description: AppendURI 변환은 데이터 집합을 작성하는 데 사용된 로그 항목에서 얻은 정보에 기본값을 추가하는 방법을 제공합니다.
solution: Analytics
title: AppendURI
topic: Data workbench
uuid: 8334d4f9-2bf6-4bd0-af65-8f2b0959652d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# AppendURI{#appenduri}

AppendURI 변환은 데이터 집합을 작성하는 데 사용된 로그 항목에서 얻은 정보에 기본값을 추가하는 방법을 제공합니다.

변환은 URI 차원을 만드는 데 사용되는 내부 필드 끝에 이름-값 쌍을 배치합니다. 이름-값 쌍은 쿼리 문자열 키 매개 변수를 이름 및 식별된 입력 매개 변수의 값으로 사용하여 만들어집니다. 이 [!DNL AppendURI] 명령은 적절한 ? 및 심볼은 이름-값 쌍을 [!DNL URI] 줄기에서 분리하고 URI에 적용될 수 있는 이전 [!DNL AppendURI] 작업과 분리하기 위해 필요합니다.

변환은 [!DNL AppendURI] 파일 또는 [!DNL Transformation.cfg] [!DNL Transformation Dataset Include] 파일에서 정의된 경우에만 작동합니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
|  이름  | 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. |  |
| 설명 | 선택 사항입니다. 변환에 대한 참고 사항. |  |
| 조건 | 이 변환이 적용되는 조건입니다. |  |
| 기본값 | 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. |  |
| 입력 | URI에 값이 추가되는 필드의 이름입니다. |  |
| 쿼리 문자열 키 | 추가할 이름-값 쌍을 만드는 데 사용할 이름입니다. |  |

기존의 모델-뷰-컨트롤러 접근 방식을 사용하여 생성된 웹 사이트를 고려해 보십시오. 이러한 시스템에서 단일 웹 페이지가 시스템에 대한 액세스 포인트가 되는 것이 일반적입니다. 이러한 사이트의 경우, 시스템의 트래픽 패턴에 대한 시각화는 매우 흥미롭지 않고 방문자 사용률 및 트래픽 흐름에 대한 통찰력을 제공하지 않습니다. 예를 들어 다음 양식의 URI를 통해 모든 웹 요청을 전송하는 웹 사이트를 생각해 보십시오.

* [!DNL http://www.examplesite.com/modelview.asp?id=login&name=bob]

modelview ASP 페이지는 모든 트래픽을 수신하고 쿼리의 ID 필드 값을 기반으로 동작을 결정합니다. 기본적으로 URI 차원은 단일 항목을 포함합니다.

* [!DNL modelview.asp]

이렇게 하면 모든 트래픽이 단일 URI를 통해 이동되기 때문에 사이트를 통한 트래픽이 다소 흥미롭지 않게 매핑됩니다. 이 특정 시나리오를 해결하고 보다 유용한 정보를 제공하는 웹 사이트의 기본 아키텍처에 제공하기 위해 cs-uri-query 필드의 고유한 이름-값 쌍 중 일부를 시각화에 사용되는 URI 차원으로 이동하는 데 사용할 [!DNL AppendURI] 수 있습니다. 아래 표시된 변환은 이러한 변환에 대한 세부 정보를 제공합니다.

![](assets/cfg_TransformationType_AppendURI.png)

이 예에서는 시스템에서 모든 요청을 처리하는 데 사용되는 두 개의 페이지가 있습니다. [!DNL modelview.asp] 및 [!DNL xmlmodelview.asp]Adobe 한 페이지는 브라우저 트래픽에 사용되고 다른 페이지는 시스템 간 XML 커뮤니케이션에 사용됩니다. 응용 프로그램 서버 프로세스에서는 cs-uri-query의 id 이름을 사용하여 수행할 작업을 결정합니다. 따라서 id 필드에서 값을 추출하여 URI에 추가할 수 있습니다. 그 결과 웹 사이트를 통한 방문자 트래픽을 반영하는 다양한 범위의 URI가 수집됩니다. 여기에서 [!DNL String Match] 조건은 관심 있는 두 웹 페이지의 cs-uri-stem 필드를 검색하여 다른 모든 페이지를 무시하여 변환이 적용되는 로그 항목을 결정합니다. 입력(이름-값 쌍의 값)은 cs-uri-query(id)의 결과로서 &quot;login&quot;입니다. 쿼리 문자열 키 매개 변수에 의해 지정된 대로 추가되는 이름은 &quot;id&quot;입니다. 따라서 예제의 들어오는 cs-uri 값에 대해 [!DNL URI] 차원에 의해 사용된 결과 URI는 [!DNL /modelview.asp&id=login]입니다.
