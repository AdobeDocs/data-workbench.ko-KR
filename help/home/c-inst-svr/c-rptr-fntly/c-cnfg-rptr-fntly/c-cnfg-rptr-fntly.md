---
description: 반복 기능을 사용하면 Insight Server FSU가 하나 이상의 소스에서 센서가 획득한 이벤트 데이터를 받아 Insight ServerReplication Service를 실행하는 하나 이상의 Insight Server FSU에 데이터를 복제할 수 있습니다.
solution: Analytics
title: 반복 기능 구성
uuid: 45dca069-a91f-4fd4-bd47-c8c2e6aab834
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 9%

---


# 반복 기능 구성{#configuring-repeater-functionality}

반복 기능을 사용하면 Insight Server FSU가 하나 이상의 소스에서 센서가 획득한 이벤트 데이터를 받아 Insight ServerReplication Service를 실행하는 하나 이상의 Insight Server FSU에 데이터를 복제할 수 있습니다.

See [Insight Server Replication Service](../../../../home/c-inst-svr/c-ins-svr-rep-svc/c-ins-svr-rep-svc.md#concept-926e654e80d943a0b6ac44a82a510d92). 이 기능을 사용하면 재해 복구를 위해 중복 시설로 데이터를 복제할 수 있습니다. 대상 서버는 네트워크 클라이언트 역할을 하며 소스 FSU에 연결하여 여러 데이터 세트에 포함하기 위해 이벤트 데이터의 복사본을 요청합니다.

방화벽이 있는 여러 레이어가 있는 네트워크 인프라에서 반복 기능을 사용하여 방화벽으로 분리된 구성 요소 간에 단일 포트를 단일 포트로 연결하는 통신을 수행할 수 있습니다.

설치, 구성 및 운영을 위한 시스템 요구 사항에 대한 자세한 내용 [!DNL Repeater]은 *최소 시스템 요구 사항* 문서를 참조하십시오.

설치하려면 다음 두 가지 절차 [!DNL Repeater]에 대해 나열된 단계를 수행해야 합니다.

* [반복을 위한 Insight Server FSU 구성](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-fsu-rptr.md#task-1ad7fa5777b845f4bd398f97226e56b2)
* [Target 컴퓨터에 대한 액세스 제어 구성](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-acc-ctrll-tgt-mach.md#task-0e49953728444839bc0a26234501a4c5)

네트워크 방화벽이 사용자 [!DNL Repeater] 의 액세스 권한을 허용하는 [!DNL Insight]경우 인사이트와 반복 간 연결 [만들기에 설명된 대로 연결을 만들 수 있습니다](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118).
