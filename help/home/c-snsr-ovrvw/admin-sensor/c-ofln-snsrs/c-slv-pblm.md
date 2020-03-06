---
description: '오류로 인해 웹 서버가 오프라인 상태가 되면 솔루션은 로그 처리 모드.cfg 파일을 열고 센서의 ID(예: WEB2)를 "오프라인 소스" 섹션에 추가할 수 있는 적절한 권한이 있는 데이터 워크벤치 사용자가 필요로 하는 간단한 솔루션입니다.'
solution: Insight
title: 문제 해결
uuid: 19d47b06-be12-4adf-9eac-b16cf7131834
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 문제 해결{#solving-the-problem}

오류로 인해 웹 서버가 오프라인 상태가 되면 솔루션은 로그 처리 모드.cfg 파일을 열고 센서의 ID(예: WEB2)를 &quot;오프라인 소스&quot; 섹션에 추가할 수 있는 적절한 권한이 있는 데이터 워크벤치 사용자가 필요로 하는 간단한 솔루션입니다.

파일의 이 섹션에서는 이 소스가 오프라인 상태이므로 더 이상 이 소스의 데이터를 기대하지 [!DNL data workbench server] 않도록 합니다.

>[!NOTE]
>
>이 변경 사항은 Adobe 컨설턴트가 수행할 필요가 없습니다. 파일을 열 수 있는 적절한 권한이 있는 사람은 누구나 [!DNL Log Processing Mode.cfg] 이 설정을 변경할 수 있습니다.

WEB2가 데이터를 다시 전송하기 시작하는 [!DNL data workbench server] 경우, 소스를 다시 온라인으로 가져오고, As Time을 조정하여 모든 소스에서 데이터를 마지막으로 받은 시간을 반영합니다. 즉, 시스템에 들어오는 새로운 데이터가 에 기록된 데이터보다 우선합니다 [!DNL Log Processing Mode.cfg file].

WEB2가 다시 오프라인 상태가 되면 기준 시간이 다시 중지되고 WEB2가 이미 오프라인 소스로 나열된 경우에도 [!DNL Log Processing Mode.cfg] 파일을 다시 편집해야 합니다. 이것은 표준시의 정의에 따라 제품 디자인의 가공물입니다.마지막으로 시스템에 알려진 모든 소스에 대한 데이터가 있는 경우

웹 서버(WEB4, WEB5, WEB6)를 더 추가하고, 웹 서버가 [!DNL data workbench server]로 데이터를 전송하기 시작하면, 새 소스를 [!DNL data workbench server] 인식할 필요가 없습니다. 시스템은 위에서 설명한 바와 같이 이러한 새로운 소스로부터 데이터를 필요로 한다는 것을 인식하게 됩니다.
