---
description: '오류로 인해 웹 서버가 오프라인으로 전환되면 솔루션은 Log Processing Mode.cfg 파일을 열고 센서의 ID(예: WEB2)를 "Offline Sources" 섹션에 추가할 적절한 권한을 가진 Data Workbench 사용자가 필요로 하는 간단한 솔루션입니다.'
title: 문제 해결
uuid: 19d47b06-be12-4adf-9eac-b16cf7131834
exl-id: 4a05dc06-360b-4c15-a881-81d350e95372
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 문제 해결{#solving-the-problem}

{{eol}}

오류로 인해 웹 서버가 오프라인으로 전환되면 솔루션은 Log Processing Mode.cfg 파일을 열고 센서의 ID(예: WEB2)를 &quot;Offline Sources&quot; 섹션에 추가할 적절한 권한을 가진 Data Workbench 사용자가 필요로 하는 간단한 솔루션입니다.

파일의 이 섹션은 [!DNL data workbench server] 실제로 오프라인 상태이므로 더 이상 이 소스의 데이터를 기대하지 않아야 합니다.

>[!NOTE]
>
>이 변경 사항은 Adobe 컨설턴트가 수행할 필요가 없습니다. 열기에 적절한 권한이 있는 사람 [!DNL Log Processing Mode.cfg] 파일이 이 변경 작업을 수행할 수 있습니다.

WEB2에서 데이터를 다시 전송하기 시작하면 [!DNL data workbench server] 소스를 다시 온라인 상태로 전환하고 알고 있는 모든 소스에서 데이터를 마지막으로 받은 시간을 반영하도록 기준 시간을 조정합니다. 즉, 시스템에 들어오는 새 데이터가 [!DNL Log Processing Mode.cfg file].

WEB2가 다시 오프라인 상태가 되면 기준 시간이 다시 중지되며, 다음을 편집해야 합니다 [!DNL Log Processing Mode.cfg] WEB2가 이미 오프라인 소스로 나열되었을 수도 있지만 파일을 다시 엽니다. 기준 시간의 정의에 따라 제품 디자인의 아티팩트입니다. 마지막으로 시스템에 알려진 모든 소스에 대한 데이터가 있는 시간입니다.

웹 서버(WEB4, WEB5, WEB6)를 더 추가하고 데이터를 [!DNL data workbench server]를 채울 필요는 없습니다 [!DNL data workbench server] 새 소스를 인식합니다. 시스템은 위에서 설명한 대로 이러한 새로운 소스의 데이터를 예상해야 한다는 것을 인식하게 됩니다.
