---
description: 센서가 오프라인으로 전환되는 것과 관련하여 두 가지 시나리오를 계획합니다.
title: 오프라인 센서 처리
uuid: a8be847d-e506-4fbc-9d57-a28ff0cbeff2
exl-id: f655c2ad-da3a-47cc-a62c-0a2937cdc0e4
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 11%

---

# 오프라인 센서 처리{#dealing-with-offline-sensors}

센서가 오프라인으로 전환되는 것과 관련하여 두 가지 시나리오를 계획합니다.

**권장 빈도:**  필요에 따라

이러한 시나리오는 웹 서버가 다른 서버에서 순환되지 않도록 하는 것이며 웹 서버가 장애 발생 때문에 완전히 다운되는 것입니다.

이해하는 첫 번째 개념은 [!DNL data workbench server]에 있는 &quot;기준&quot; 시간입니다.
