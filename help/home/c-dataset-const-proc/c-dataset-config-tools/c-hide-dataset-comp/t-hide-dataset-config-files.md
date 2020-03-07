---
description: 내부 또는 상속된 다른 프로파일에서 구성 파일을 상속하지 않으려는 경우(즉, 데이터세트 구성 동안 파일의 지침을 무시해야 함), 파일을 수정하지 않으려면 같은 이름의 빈(0바이트) 파일을 만들고 다른 프로필에 저장할 수 있습니다.
solution: Analytics
title: 데이터 집합 구성 파일 숨기기
topic: Data workbench
uuid: eb33cf54-e067-4af2-a10e-7ffe43910e4f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 집합 구성 파일 숨기기{#hiding-dataset-configuration-files}

내부 또는 상속된 다른 프로파일에서 구성 파일을 상속하지 않으려는 경우(즉, 데이터세트 구성 동안 파일의 지침을 무시해야 함), 파일을 수정하지 않으려면 같은 이름의 빈(0바이트) 파일을 만들고 다른 프로필에 저장할 수 있습니다.

**데이터 세트 구성 파일 0바이트**

1. 에서 [!DNL Profile Manager]필요한 폴더 및 하위 폴더를 열어 0바이트에서 사용할 파일을 찾습니다.
1. 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Make Local]**.
1. 메모장과 같은 텍스트 편집기에서 로컬 파일을 열고 콘텐트를 삭제합니다.
1. 파일을 저장하고 닫습니다.
1. 에서 0 [!DNL Profile Manager]바이트 파일을 원본 파일이 있는 프로필의 오른쪽에 있는 프로필에 저장합니다. 0바이트 파일이 원본 파일보다 우선합니다.

   열에서 확인 표시 대신 하이픈(-) [!DNL Profile Manager]은 아래 예와 같이 0바이트 파일을 식별합니다.

   ![](assets/vis_ProfileManager_ZeroByteFile.png)

데이터 세트를 다시 처리할 때 데이터 세트에 원본 파일이 정의하는 데이터 세트 구성 요소가 포함되어 있지 않습니다.

>[!NOTE]
>
>시각화 또는 지표 정의에 사용되는 확장 차원을 정의하는 구성 파일을 0바이트로 지정하면 데이터 워크벤치에서 해당 시각화 또는 지표에 대한 오류를 각각 생성합니다.

또한 0바이트 파일을 사용하여 지표, 차원 또는 필터를 프로필의 다른 위치로 이동하거나 메뉴 항목을 숨길 수 있습니다. For information, see the *Data Workbench User Guide*.