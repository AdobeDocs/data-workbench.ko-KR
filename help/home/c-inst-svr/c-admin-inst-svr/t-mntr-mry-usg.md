---
description: 주소 공간 로드 평가 및 모니터링에 대한 정보입니다.
title: 메모리 사용 모니터링
uuid: e7f1c51b-d874-43f4-a074-1c064b5f298a
exl-id: b8c0b33b-dbec-4947-911b-11c8a83bbc9c
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 2%

---

# 메모리 사용 모니터링{#monitoring-memory-usage}

주소 공간 로드 평가 및 모니터링에 대한 정보입니다.

**주소 공간 로드 모니터링**

**권장 빈도:** 일별

주소 공간 로드는 올바르게 구성된 [!DNL Insight Server]에서 사용하는 최대 주소 공간의 분수를 측정합니다. 구성 매개 변수를 변경하여 메모리 사용을 줄이더라도 일반적으로 [!DNL Insight Server] 서비스를 다시 시작할 때까지 감소되지 않습니다.

주소 공간 사용률이 예상치 못한 증가를 설명하기 위해 주소 공간 로드 최대값에 안전 여백이 내장되어 있습니다. 이 안전 마진을 일부러 잘라서는 안 된다. 이것은 응급 상황용이며 Adobe 애플리케이션에 추가된 기능을 지원하지 않습니다.

>[!NOTE]
>
>더 많은 주소 공간을 사용할 수 있도록 하고 메모리 소모 오류를 방지하려면 운영 체제에서 /3GB 스위치를 사용할 수 있도록 설정되어 있고 Low Fragmentation Heap이 작동 중인지 확인하십시오.

[!DNL Insight Server] 이벤트 데이터 로그에 기록된 오류는 주소 공간 로드로 인해 문제가 발생한다는 단서를 제공할 수 있습니다.

* &quot;요청한 X바이트 블록이 너무 큽니다.&quot; 오류는 주소 공간 로드, 성능 및 네트워크 대역폭에 과도한 영향을 줄 수 있음을 나타냅니다. 이러한 큰 블록은 많은 메모리를 사용하고 주소 공간의 연속적인 큰 블록을 필요로 하여 주소 공간 사용에 크게 기여할 수 있습니다.

   이 문제를 해결하려면 가장 큰 차원의 카디널리티를 줄여 주소 공간 로드를 늘릴 수 있습니다. 차원의 카디널리티를 줄일 수 없는 경우 예기치 않은 증가를 처리할 수 있도록 주소 공간 로드를 충분히 작게 유지해야 합니다.
* &quot;메모리 예산이 초과됨&quot; 오류는 쿼리 메모리 제한을 늘려야 할 수도 있음을 나타냅니다. 쿼리에 사용되는 메모리는 차원 카디널리티에 비례하며 경우에 따라 요소 이름의 길이가 달라집니다. 쿼리 메모리 제한을 늘리면 총 주소 공간 로드를 늘리고 큰 크기를 줄입니다.

>[!NOTE]
>
>기본적으로 큰 페이지를 사용할 수 있으며 메모리 매핑 조회를 사용할 수 없습니다. DWB 6.7 이상에서는 데이터 세트 구성에서 변경할 수 있습니다. 변경 사항이 있으면 서버를 다시 시작해야 합니다.

**주소 공간 로드를 평가하려면**

시스템의 주소 공간 로드를 정확하게 평가하려면 데이터 세트를 재처리하고 나중에 [!DNL Insight Server]을 다시 시작하지 않고 일부 일반 쿼리를 수행한 다음 이러한 단계를 수행하여 측정된 주소 공간 로드를 보는 것이 좋습니다.

[!DNL Insight Server]이(가) 마지막으로 다시 시작된 후 다시 처리되지 않고 심각하게 쿼리되지 않은 경우 주소 공간 로드에서 결론을 도출하지 않아야 합니다.

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.
1. 구성할 [!DNL Insight Server] 아이콘을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Detailed Status]** 를 클릭합니다.
1. 세부 상태 인터페이스에서 **[!UICONTROL Memory Status]** 을 클릭하여 해당 콘텐츠를 확인합니다. 주소 공간 로드 매개 변수에서 백분율로 표현되는 주소 공간 부하 및 상태를 나타내는 상위 설명을 볼 수 있습니다.

   다음 표는 주소 공간 로드에 대한 범위 및 상태를 보여 줍니다. 각 범위에 대한 권장 작업이 나열됩니다.

   | 주소 공간 로드(%) | 상태 | 권장 작업 |
   |---|---|---|
   | 0-15 | 무정하 | 없음. |
   | 15-33 | light | 없음. |
   | 33-66 | 중재 | 없음. |
   | 66-100 | 무겁고 | 메모리 소모 실패를 방지하기 위해 중요한 추가 기능을 추가하거나 더 많은 데이터를 처리하려고 시도하지 마십시오. |
   | 100년 125월 | 신뢰성 저하 | 데이터 집합 구성을 조정하여 주소 공간 로드를 줄이십시오. |
   | 125 이상 | 실패 | 데이터 집합 구성을 조정하여 주소 공간 로드를 줄이십시오. 장애가 발생하기 전에 장애 발생 가능 상태가 표시되지 않을 수 있습니다. |

   주소 공간 로드가 100%를 초과하는 것이 표시되면 가능한 한 빨리 구성을 변경하여 주소 공간 사용을 줄여야 합니다.
