---
description: 웹 서버에서 실행 중인 웹 서버 인스턴스가 하나 있는 센서의 일반 구성에 대한 정보입니다.
title: 웹 서버의 여러 인스턴스 작업
uuid: 778ea95f-e0f2-4c2a-b7ed-7e323fea1e48
exl-id: a371f9ed-6c27-4b3d-843f-ae5621013410
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 5%

---

# 웹 서버의 여러 인스턴스 작업{#working-with-multiple-instances-of-a-web-server}

{{eol}}

웹 서버에서 실행 중인 웹 서버 인스턴스가 하나 있는 센서의 일반 구성에 대한 정보입니다.

![](assets/web_inst.png)

이 시나리오에서는 단일 웹 서버 인스턴스가 메모리 매핑된 큐 파일에 데이터를 기록하고 있으며, 이 파일은 전송기가 읽고 로 전송됩니다 [!DNL data workbench server].

When [!DNL Sensor] 는 여러 컬렉터 인스턴스를 실행하는 웹 서버에 설치되어 있으므로 다음 두 가지 방법 중 하나를 사용하여 구성할 수 있습니다.

* 모든 컬렉터 모듈이 하나의 큐 파일을 공유할 수 있습니다.

   단일 큐 파일을 사용하는 경우 아키텍처 자체가 덜 복잡하므로 관리, 구성 및 관리가 다소 간소화됩니다. 그러나 단일 큐 파일을 사용하면 인스턴스 수에 관계없이 전체 웹 서버가 WEB1로 식별됩니다.

* 위의 아키텍처를 여러 번 복제하고 각 웹 서버 인스턴스에 별도의 큐 파일이 있도록 할 수 있습니다.

   이렇게 하면 각 웹 서버 인스턴스를 고유하게 식별할 수 있습니다. 즉, 웹 서버(및 [!DNL Sensor] configuration)은 이 구성의 함수입니다.

어떤 경우든, 데이터에 여전히 모든 호스트 이름 정보가 있으므로 [!DNL www.client.com], [!DNL www2.client.com]등. 올바른 구성은 분석 목표 및 분석가가 웹 서버에서 실행되는 특정 인스턴스를 기반으로 데이터를 세그먼트화해야 하는지 여부에 따라 결정됩니다.

>[!NOTE]
>
>이러한 유형의 세그먼테이션은 일반적으로 운영 분석에서만 사용되며 해당 영역 외부에서 많은 실용적인 사용을 제공하지 않습니다.
