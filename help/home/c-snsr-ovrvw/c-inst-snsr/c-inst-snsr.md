---
description: 활동을 측정하려는 서버와 동일한 컴퓨터에 센서를 설치합니다.
title: 센서 설치
uuid: 8d500fd0-daa0-453b-8284-b3f112a358ce
exl-id: cd5b54bf-301a-41a9-a69c-d9adb314be03
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# 센서 설치{#installing-sensor}

활동을 측정하려는 서버와 동일한 컴퓨터에 센서를 설치합니다.

이벤트 데이터를 캡처할 각 서버는 [!DNL Sensor]을 실행해야 합니다.

[!DNL Sensor] 은 지원되는 다양한 웹 및 애플리케이션 서버 또는 측정용으로 태그가 지정된 페이지, 광고 및 기타 인터넷 객체에서 정보를 획득하는 데 사용되는 전문 데이터 수집 서버에 설치할 수 있습니다.

>[!NOTE]
>
>[!DNL Sensor] 은 올바르게 구성된 웹, 애플리케이션 또는 데이터 수집 서버의 성능을 저하시키지 않습니다.

Adobe은 Microsoft Windows, AIX, Linux 및 Solaris를 포함하되 이에 제한되지 않는 공통 운영 체제에서 실행되는 AOLServer, Apache, iPlanet, JBoss, Microsoft IIS, Netscape Enterprise, Tomcat 및 Weblogic을 포함하되 이에 국한되지 않는 광범위한 웹 및 J2EE 애플리케이션 서버 제품군을 지원하기 위해 [!DNL Sensor]를 설계했습니다. [!DNL Sensor’s] 모듈식 아키텍처를 통해 Adobe은 필요에 따라 다른 애플리케이션을 위한 새로운 데이터 획득 로직을 매우 신속하게 생성할 수 있습니다.

이 장에는 웹 서버/운영 체제 조합을 위한 [!DNL Sensor] 설치 절차가 포함되어 있습니다.

[!DNL Sensor]에서 데이터를 수집하는 [!DNL data workbench server]을 아직 설치하지 않은 경우 이 장의 절차를 수행하기 전에 반드시 설치해야 합니다.
