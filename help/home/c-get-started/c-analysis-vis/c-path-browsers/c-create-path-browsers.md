---
description: 그래프, 표 또는 프로세스 맵에서 경로 브라우저를 만들 수 있습니다.
solution: Analytics
title: 경로 브라우저 만들기
topic: Data workbench
uuid: 84a5e587-fb02-461b-aec8-1b6ad473ebc3
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 경로 브라우저 만들기{#creating-path-browsers}

그래프, 표 또는 프로세스 맵에서 경로 브라우저를 만들 수 있습니다.

**그래프 또는 표에서 경로 브라우저를 만들려면**

1. 작업 영역에 경로 브라우저를 추가합니다. 왼쪽 상단 모서리의 레이블(시퀀스...)을 제외하고 시각화는 비어 있습니다.
1. 경로 브라우저에 표시할 요소의 차원을 보여주는 그래프 또는 표를 엽니다. 예를 들어 웹 사이트 데이터를 사용하여 작업하는 경우 페이지 그래프나 표를 열고 루트로 설정할 페이지를 식별합니다.
1. Ctrl+Alt를 누르고 원하는 요소를 경로 브라우저로 드래그합니다. 경로 브라우저의 왼쪽 위 모서리에 있는 레이블은 요소를 경로 브라우저로 드래그하는 기본 차원을 반영하도록 변경됩니다.

>[!NOTE]
>
>요소를 경로 브라우저로 드래그하면 경로 브라우저와 연결된 기본 차원이 변경될 수 있지만 수준 차원, 그룹 차원 또는 지표는 변경되지 않습니다. 따라서 경로 브라우저의 수준 차원, 그룹 차원 및 지표와 함께 사용할 때 의미가 있는 기본 차원을 선택할 때는 주의해야 합니다. 수준 차원, 그룹 차원 또는 지표를 변경하려면 메모장과 같은 텍스트 편집기에서 경로 브라우저의 [!DNL *.vw] 파일을 편집해야 합니다. 경로 [브라우저 구성을 참조하십시오](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-path-brwsr.md#task-bbb3ddaa140a414f984b697c2b8202a3).

**프로세스 맵에서 경로 브라우저를 만들려면**

>[!NOTE]
>
>프로세스 맵에서 생성된 경로 브라우저는 프로세스 맵에 표시된 요소만 표시합니다. 기본 차원의 다른 요소는 표시되지 않습니다.

1. 프로세스 맵을 만듭니다. 프로세스 [맵 만들기를 참조하십시오](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-create-proc-maps.md#concept-daf5b14dae7a442191611b1b9c1122bf).
1. 프로세스 맵에서 원하는 요소를 경로 브라우저로 드래그합니다. 요소는 경로 브라우저의 루트가 됩니다.

>[!NOTE]
>
>프로세스 맵에서 경로 브라우저를 만들 때 경로 브라우저는 연관된 기본 차원 요소가 없는 레벨 차원의 요소를 무시합니다. 프로세스 맵에서 경로 브라우저로 노드를 드래그하면 경로 브라우저의 기본 차원(맵이라는 이름)이 프로세스 맵에 의해 정의되고 해당 요소는 프로세스 맵의 요소로 제한됩니다. 따라서 경로 브라우저 수준 차원의 일부 요소에는 연결된 기본 차원 요소가 없으며 경로 브라우저에 표시되지 않습니다.
