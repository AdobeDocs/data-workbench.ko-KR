---
description: 실험에서는 제어 그룹 외에 테스트 그룹 수를 정의할 수 있습니다.
solution: Analytics,Analytics
title: 통제 실험은 어떻게 작동합니까?
topic: Data workbench
uuid: 9549e2ab-dca9-4fb1-9729-65072f951900
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---


# 통제 실험은 어떻게 작동합니까?{#how-do-controlled-experiments-work}

실험에서는 제어 그룹 외에 테스트 그룹 수를 정의할 수 있습니다.

실험이 실행될 때 웹 사이트의 모든 방문자는 테스트 그룹 또는 제어 그룹의 일부로 실험 관련 페이지에 액세스하는 즉시 실험의 일부가 됩니다. 방문자는 실험 구성 중에 정의된 비율로 임의로 실험 그룹에 할당됩니다.

제어된 실험은 웹 클러스터의 각 컨텐트 서버에 설치된 [!DNL Sensor] 소프트웨어를 사용하여 구현됩니다. 컨텐츠 서버가 요청을 수신하면 테스트 그룹의 방문자를 임의로 [!DNL Sensor] 선택하고 해당 페이지 요청을 실험 컨텐츠로 리디렉션합니다. 테스트 컨텐츠를 볼 방문자를 선택하면 주소 표시줄이 원래 요청한 URI를 계속 나열하지만 방문자는 테스트 URI로 라우팅됩니다. [!DNL Sensor] 이 프로세스는 서버 애플리케이션에서 내부적으로 수행되므로 사용자는 테스트 시기를 알지 못하며, 이는 공정한 실험을 위한 중요한 고려 사항입니다.

[!DNL Sensor] 분석에 사용할 로그 파일에 원본 URI가 아닌 테스트 URI를 전달합니다.

실험한 가설이 맞는지를 확인하기 위해 실험 결과 [!DNL Insight] 를 쉽게 분석할 수 있다.

>[!NOTE]
>
>Adobe은 분석 데이터 세트를 구성 및 유지 관리하는 조직의 개인 사용자의 의견을 통해 제어되는 실험을 조정 및 수행할 것을 적극 권장합니다.

