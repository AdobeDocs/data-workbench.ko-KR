---
description: 표시된 요소를 루트로 지정하거나 시각화에 새 요소를 추가하여 경로 브라우저의 루트를 변경할 수 있습니다.
solution: Analytics
title: 경로 브라우저의 루트 변경
topic: Data workbench
uuid: 0bb9b004-9736-411b-bd22-cac04f4733a6
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 경로 브라우저의 루트 변경{#change-the-path-browser-s-root}

표시된 요소를 루트로 지정하거나 시각화에 새 요소를 추가하여 경로 브라우저의 루트를 변경할 수 있습니다.

>[!NOTE]
>
>시작 또는 종료 노드를 경로 브라우저의 루트로 설정할 수 없습니다.

**경로 브라우저의 루트를 설정하려면**

* 원하는 요소를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Set as root]**&#x200B;클릭합니다.

**경로 브라우저에 새 요소를 추가하려면**

1. 경로 브라우저에 표시할 요소의 차원을 보여주는 그래프 또는 표를 엽니다.

   예를 들어 웹 사이트 데이터를 사용하여 작업하는 경우 페이지 그래프나 표를 열고 루트로 설정할 페이지를 식별합니다.

1. Ctrl+Alt를 누르고 원하는 요소를 경로 브라우저의 루트 위치로 드래그합니다.

   >[!NOTE]
   >
   >원하는 차원의 요소를 경로 브라우저로 드래그하여 경로 브라우저와 연결된 기본 차원을 변경할 수 있습니다. 이 요소는 경로 브라우저의 새 루트가 되며, 경로 브라우저의 왼쪽 위 모서리에 있는 레이블은 이 요소의 차원을 반영하도록 변경됩니다.

   예를 들어 각 세션의 페이지 시퀀스를 표시하는 페이지 경로 브라우저를 만든다고 가정합니다. 검색어 차원의 요소를 경로 브라우저로 드래그하면 검색어 요소가 새 루트가 되고 레이블에 각 세션에 대한 검색어 시퀀스가 표시됩니다.

   >[!NOTE]
   >
   >요소를 경로 브라우저로 드래그하면 경로 브라우저와 연결된 기본 차원이 변경될 수 있지만 수준 차원, 그룹 차원 또는 지표는 변경되지 않습니다. 따라서 경로 브라우저의 수준 차원, 그룹 차원 및 지표와 함께 사용할 때 의미가 있는 기본 차원을 선택할 때는 주의해야 합니다. 수준 차원, 그룹 차원 또는 지표를 변경하려면 메모장과 같은 텍스트 편집기에서 경로 브라우저의 [!DNL *.vw] 파일을 편집해야 합니다. 경로 [브라우저 구성을 참조하십시오](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-path-brwsr.md#task-bbb3ddaa140a414f984b697c2b8202a3).
