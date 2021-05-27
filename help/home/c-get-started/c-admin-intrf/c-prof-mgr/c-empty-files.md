---
description: 프로필에서 파일을 삭제할 수 있는 권한이 없거나 파일을 영구적으로 삭제하지 않으려는 경우 빈(0바이트) 파일을 사용하여 파일을 숨길 수 있습니다.
title: 비우고 파일 숨기기(0바이트)
uuid: 82c1a5c9-1bbb-41c7-bee7-704f0a9ef87d
exl-id: d5841fb5-afae-4352-aded-01b0b2eb9f85
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 4%

---

# 비우고 파일 숨기기(0바이트){#hide-a-file-by-emptying-it-zero-byte}

프로필에서 파일을 삭제할 수 있는 권한이 없거나 파일을 영구적으로 삭제하지 않으려는 경우 빈(0바이트) 파일을 사용하여 파일을 숨길 수 있습니다.

[!DNL Profile Manager]에서 열의 확인 표시 대신 하이픈(-)은 0바이트 파일을 식별합니다.

![](assets/vis_ProfMgr_Zero-byte.png)

파일을 숨기는 다른 방법(예: [!DNL order.txt], Show 매개 변수 및 Hidden 매개 변수)과 달리, Data Workbench은 0으로 작성된 파일을 존재하지 않는 것으로 처리합니다. 예를 들어 시각화 또는 지표 정의에 사용된 Data Workbench을 0바이트로 지정하면 해당 시각화 또는 지표에 대해 각각 오류가 발생합니다.

이 기능은 다음을 수행하려는 시기를 포함하여 여러 가지 이유로 유용합니다.

* **파일을 삭제하는** 데 필요한 프로필 권한이 없어도 Data Workbench에서 파일을 사용 불가능하게 만듭니다.
* **원래 위치에서 파일** 을 삭제하는 데 필요한 프로필 권한이 없어도 지표, 차원 또는 필터를 다른 위치로 이동합니다.
* **메뉴 항목을 숨깁니다.** 예를 들어  [!DNL Base] 파일에  [!DNL Metric Legend] 가 정의되어  [!DNL Metric.vw] 있습니다. 회사가 범례 추가 > 지표 하위 메뉴에 표시할 3개의 지표 범례를 생성했다고 가정합니다. [!DNL Base] 프로필 [!DNL Metric.vw] 파일을 0바이트로 만들 수 있으므로 새 하위 메뉴 및 3개의 새 지표 범례가 표시됩니다.

**파일을 숨기려면**

1. [!DNL Profile Manager]에서 필요한 폴더와 하위 폴더를 열어 0바이트로 지정할 파일을 찾습니다.
1. 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다.
1. 로컬 파일을 열고 해당 컨텐츠를 삭제합니다.
1. 파일을 저장하고 닫습니다.
