---
description: 반복 기능을 사용하면 Insight Server FSU에서 하나 이상의 소스에서 센서가 획득한 이벤트 데이터를 수신하고 해당 데이터를 Insight Server 복제 서비스를 실행하는 하나 이상의 Insight Server FSU에 복제할 수 있습니다.
title: 반복 기능 구성
uuid: 45dca069-a91f-4fd4-bd47-c8c2e6aab834
exl-id: 61b70772-07fb-4963-b09f-6b2cf97b01a1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 9%

---

# 반복 기능 구성{#configuring-repeater-functionality}

반복 기능을 사용하면 Insight Server FSU에서 하나 이상의 소스에서 센서가 획득한 이벤트 데이터를 수신하고 해당 데이터를 Insight Server 복제 서비스를 실행하는 하나 이상의 Insight Server FSU에 복제할 수 있습니다.

[Insight Server 복제 서비스](../../../../home/c-inst-svr/c-ins-svr-rep-svc/c-ins-svr-rep-svc.md#concept-926e654e80d943a0b6ac44a82a510d92)를 참조하십시오. 이 기능을 사용하면 재해 복구를 위해 중복 시설로 데이터를 복제할 수 있습니다. 대상 서버는 네트워크 클라이언트 역할을 하며 소스 FSU에 연결하여 여러 데이터 세트에 포함하기 위해 이벤트 데이터의 사본을 요청합니다.

여러 계층의 방화벽이 있는 네트워크 인프라에서 반복 기능을 사용하여 방화벽에 의해 분리된 구성 요소 간에 단일 포트-단일 포트 통신을 수행할 수 있습니다.

[!DNL Repeater] 설치, 구성 및 운영을 위한 시스템 요구 사항에 대한 자세한 내용은 *최소 시스템 요구 사항* 문서를 참조하십시오.

[!DNL Repeater]을 설치하려면 다음 두 절차에 대해 나열된 단계를 수행해야 합니다.

* [반복을 위한 Insight Server FSU 구성](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-fsu-rptr.md#task-1ad7fa5777b845f4bd398f97226e56b2)
* [Target 컴퓨터에 대한 액세스 제어 구성](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-acc-ctrll-tgt-mach.md#task-0e49953728444839bc0a26234501a4c5)

네트워크 방화벽이 [!DNL Insight]에서 [!DNL Repeater]에 액세스할 수 있는 경우 [Insight와 반복 간의 연결 만들기](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)에 설명된 대로 연결을 만들 수 있습니다.
