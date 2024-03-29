---
description: 일반적인 사이트 구성은 쿠키를 사용하여 웹 사이트 방문자를 고유하게 식별하고 시간이 지남에 따라 해당 동작을 추적합니다.
solution: Analytics
title: 사이트는 방문자를 어떻게 식별합니까?
uuid: e1e451b8-e827-4010-bda9-9147c3b09958
exl-id: 2783ee11-6d6a-463d-86b5-dd63e490201f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 3%

---

# 사이트는 방문자를 어떻게 식별합니까?{#how-does-site-identify-visitors}

{{eol}}

일반적인 사이트 구성은 쿠키를 사용하여 웹 사이트 방문자를 고유하게 식별하고 시간이 지남에 따라 해당 동작을 추적합니다.

특정 브라우저(방문자로 간주됨)가 처음으로 웹 사이트를 요청하면, [!DNL Sensor] 는 기본적으로 웹 서버와 함께 영구 쿠키를 설정합니다 [!DNL cs(cookie)(v1st)]). [!DNL x-trackingid]. 이 쿠키는 해당 방문자가 웹 사이트에 수행한 첫 번째 요청에서 한 번만 설정됩니다. 그런 다음 브라우저가 나중에 웹 사이트의 요청(페이지 또는 포함된 개체 요청)을 수행할 때마다 해당 방문자로부터 수집됩니다.

영구적 쿠키를 수락하는 것은 브라우저의 재량에 따라 결정됩니다. 사용자가 영구 쿠키를 차단하도록 선택하면 해당 페이지 보기 요청이 여전히 기록되지만, IP 및 UserAgent 필드에서 해시 변환 사용과 같이 방문자 식별 대체 방법을 구현하지 않는 한 해당 요청의 측정 데이터는 웹 사이트의 특정 방문자 또는 해당 세션과 상관관계가 없습니다.

>[!NOTE]
>
>사용 중인 방문자 식별 방법이 다음과 같은 데이터 세트에서만 사이트 실험을 분석할 수 있습니다 [!DNL Sensor] 영구적 쿠키 방법을 설정합니다. J2EE 서버(JBoss, Tomcat, WebLogic 및 WebSphere)에서 실행되는 센서는 통제 실험을 지원하지 않습니다.

통제된 실험 중에 쿠키를 수락하지 않는 사용자는 한 클릭에서 다음 클릭으로 다른 실험 그룹에 배치할 수 있습니다. 중단된 세션 필터가 꺼져 있는 상태로 테스트 분석을 수행하는 경우에만 문제가 됩니다 [!DNL Insight]: 어떤 Adobe이 권장되지 않습니다.

중단된 세션 필터에 대한 자세한 내용은 *를 참조하십시오. [!DNL Insight] 사용 안내서*.

방문자가 실험 중에 쿠키를 삭제하는 경우 방문자에게 새 쿠키가 할당되고 다른 그룹에 할당될 수 있습니다. Adobe이 방문자를 새로운 방문자로 식별하므로 이 실험은 무효화되지 않습니다.
