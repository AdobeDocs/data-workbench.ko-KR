---
description: 확장 차원을 생성하고 데이터 세트 구성의 변환 단계 동안 생성을 위해 정의할 수 있는 확장 차원 유형을 설명하는 지침입니다.
title: 확장된 차원
uuid: 465682c2-5b08-4b94-817f-ff7b405142af
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# 확장된 차원{#extended-dimensions}

확장 차원을 생성하고 데이터 세트 구성의 변환 단계 동안 생성을 위해 정의할 수 있는 확장 차원 유형을 설명하는 지침입니다.

파생 차원은 Insight Server에서 사용하는 다른 차원 카테고리를 구성합니다. 이름에서 알 수 있듯이 파생된 차원은 기존 확장 차원 또는 지표에서 만들어집니다. 확장 차원을 수행하듯이 [!DNL Transformation Dataset Configuration] 파일 내에 파생 차원을 정의하지 않습니다. 대신 상속된 프로필 또는 데이터 세트 프로필 내에서 개별 [!DNL .dim] 파일로 정의합니다.

파생 차원을 만드는 단계는 [확장 Dimension](https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/profile-mgr/c-dvrd-dim.html) 을 참조하십시오.
