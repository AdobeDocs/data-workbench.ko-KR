---
description: '오류로 인해 웹 서버가 오프라인 상태가 되면 솔루션은 로그 처리 모드.cfg 파일을 열고 센서의 ID(예: WEB2)를 "오프라인 소스" 섹션에 추가할 수 있는 적절한 권한이 있는 Data Workbench 사용자가 필요로 하는 간단한 솔루션입니다.'
title: 문제 해결
uuid: 19d47b06-be12-4adf-9eac-b16cf7131834
exl-id: 4a05dc06-360b-4c15-a881-81d350e95372
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 문제 해결{#solving-the-problem}

오류로 인해 웹 서버가 오프라인 상태가 되면 솔루션은 로그 처리 모드.cfg 파일을 열고 센서의 ID(예: WEB2)를 &quot;오프라인 소스&quot; 섹션에 추가할 수 있는 적절한 권한이 있는 Data Workbench 사용자가 필요로 하는 간단한 솔루션입니다.

이 파일 섹션에는 [!DNL data workbench server]이(가) 실제로 오프라인 상태이므로 더 이상 이 소스의 데이터를 기대하지 않도록 합니다.

>[!NOTE]
>
>이 변경 사항은 Adobe 컨설턴트가 수행할 필요가 없습니다. [!DNL Log Processing Mode.cfg] 파일을 열 수 있는 적절한 권한이 있는 사람은 이 변경 사항을 만들 수 있습니다.

WEB2가 데이터를 다시 전송하기 시작하는 경우 [!DNL data workbench server]은 소스를 다시 온라인으로 가져오고 [기준 시간]을 조정하여 알고 있는 모든 소스에서 데이터를 마지막으로 받은 시간을 반영합니다. 즉, 시스템에 들어오는 새 데이터가 [!DNL Log Processing Mode.cfg file]에 기록된 데이터보다 우선합니다.

WEB2가 다시 오프라인 상태가 되면, 기준 시간이 다시 중지되고, WEB2가 이미 오프라인 소스로 나열되었을 수도 있지만 [!DNL Log Processing Mode.cfg] 파일을 다시 편집해야 합니다. 시간 기준 정의에 따라 제품 디자인의 가공물입니다.시스템에서 알려진 모든 소스에 대한 데이터가 마지막으로 있는 시간입니다.

웹 서버(WEB4, WEB5, WEB6)를 더 추가하고 해당 서버에서 [!DNL data workbench server]에 데이터를 보내기 시작하면 [!DNL data workbench server]에서 새 소스를 인식하도록 할 필요가 없습니다. 시스템은 위에서 설명한 바와 같이 이러한 새로운 소스의 데이터를 예상해야 한다는 것을 인식하게 됩니다.
