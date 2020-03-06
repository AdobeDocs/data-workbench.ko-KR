---
description: 웹 서버 회전이 중지되거나 웹 서버가 실패한 경우 등 웹 서버 문제를 해결하는 방법에 대한 정보입니다.
solution: Insight
title: 원인 이해
uuid: a2801040-c859-4bf8-90d7-daf3d4f633f3
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 원인 이해{#understanding-the-causes}

웹 서버 회전이 중지되거나 웹 서버가 실패한 경우 등 웹 서버 문제를 해결하는 방법에 대한 정보입니다.

## 웹 서버를 순환에서 제거할 때 {#section-b9f709099cb44b4f9d1acb38ca5330e3}

웹 서버가 서버 풀에서 순환되지 않고, 주기적인 하트비트를 전송하는 송신기와 연결되어 있는 경우, 기준 시간은 최신 상태로 유지되며, 다른 사용자의 부분에 개입할 필요가 없습니다.

## 웹 서버 실패 시 {#section-19280cf83ca44bd7b1ee11bfc74494d2}

심각한 실패로 인해 웹 서버가 완전히 오프라인이거나 데이터 또는 하트비트를 전송하지 않는 경우, [!DNL data workbench server] 중단 시 현재 시간은 해당 서버가 알고 있는 모든 데이터 소스에서 데이터를 마지막으로 [!DNL data workbench server] 받은 시간을 나타냅니다. 시스템 자체는 데이터 워크벤치에서 여전히 분석에 사용할 수 있는 데이터를 계속 처리하지만 기준 시간을 기반으로 하는 [!DNL data workbench server] 모든 데이터가 작동하지 않습니다. 예를 들어, 기준 시간은 보고를 트리거하며 시스템에서 많은 파생된 차원을 만드는 데 사용됩니다. 기준 시간이 중지되면 보고가 트리거되지 않고 이러한 특정 파생 차원을 사용할 수 없습니다.

예를 들어, 6월 15일에 WEB2가 오프라인으로 전환하고 5일 동안 데이터를 전송하지 않은 경우, 기준 시간은 6월 15일 이후입니다. 예를 들어 오늘 날짜가 6월 20일임에도 불구하고 어제 차원은 6월 14일이 됩니다.