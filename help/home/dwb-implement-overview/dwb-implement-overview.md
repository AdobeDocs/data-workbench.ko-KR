---
description: Data Workbench 구현 안내서는 구현에 대한 온보딩, 계획 및 기술 질문에 대한 참조 역할을 합니다.
title: Adobe Data Workbench 구현
uuid: 2ea3ef17-29d3-4a68-9444-d9682a773942
exl-id: 12eb484c-74d6-46a9-b668-72b501f209e8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 1%

---

# Adobe Data Workbench 구현{#implementing-adobe-data-workbench}

{{eol}}

Data Workbench 구현 안내서는 구현에 대한 온보딩, 계획 및 기술 질문에 대한 참조 역할을 합니다.

DWB(Adobe Data Workbench)은 AAP(Adobe Analytics Premium)의 구성 요소입니다. 비즈니스 전문가, 데이터 분석가 및 시스템 설계자를 위해 실시간, 다차원 지표 분석, 동적 세그멘테이션, 고급 데이터 시각화 및 확장된 분석 기능을 제공하는 강력하고 확장성이 뛰어난 시각적 분석 및 보고 애플리케이션입니다. DWB는 모든 데이터 채널과 상호 작용할 수 있는 방법을 분석하여 회사의 비즈니스 목표의 효과를 측정하고, 트렌드를 정의하고, 예측을 위한 예측 모델을 생성하고, 비즈니스 프로세스를 최적화하여 성능을 향상시킬 수 있습니다. 여러 채널의 데이터를 분석함으로써 고객 행동에 대한 전체 보기를 생성하고 조직 전체에서 실행 가능한 응답을 식별할 수 있습니다.

DWB는 조직의 요구 사항에 맞게 사용자 지정된 AAP의 구성 가능한 분석 툴입니다. DWB를 사용하면 구조화된 데이터의 모든 유형을 시각화할 수 있고, 전체 데이터 세트에 대해 쿼리를 수행할 수 있으므로 방대한 양의 데이터를 실시간으로 사용자 지정 및 임시 분석할 수 있는 기능을 제공합니다. 그런 다음 필요한 보고서를 생성하여 필요할 때 배달하도록 설정하고 예약할 수 있습니다.

DWB는 다음을 제공합니다.

* 멀티채널 실시간 데이터 상관 관계
* 여러 소스에서 유연한 데이터 수집
* 강력한 고급 데이터 시각화`<discoiqbr>`

Data Workbench 구현에는 다음 단계가 포함됩니다.

1. Data Workbench에 대한 온보딩 작업
1. 검색 및 요구 사항
1. 설치 및 프로비저닝
1. 아키텍처 설정
1. 관리 설정
1. 구성
1. 구현 후

## DWB 온보딩 {#section-dc2618f7d1a74d7d8fdba163e4101e44}

이러한 온보딩 지침은 컨설팅 서비스 없이 Adobe 관리 서비스를 사용하여 단일 보고서 세트로 Data Workbench을 구현하는 고객을 위한 것입니다. Analytics Data Workbench 및 Analytics Premium을 처음 사용하는 경우 Adobe 온보딩 팀이 초기 연락처가 됩니다. 표준 Adobe Analytics 또는 이전 버전의 DWB에서 업그레이드하는 경우 Adobe 고객 성공 관리자에게 연락하여 초기 온보딩 프로세스를 시작합니다.

자세한 내용은 [DWB 온보딩](../../home/dwb-implement-overview/dwb-implement-provision/dwb-implement-onboarding.md#concept-e93aba41b26a410f959c5ca7f8e33355) 섹션을 참조하십시오.

## DWB 검색 및 요구 사항 {#section-d49b77576f57427598e366c6accfe6f4}

Data Workbench에서 솔루션을 구축하는 데 필요한 질문 및 작업에 대한 입력을 수집합니다.

자세한 내용은 [검색 및 요구 사항](../../home/dwb-implement-overview/dwb-implement-discovery.md#concept-1544d4864e9e437bbd11b1380c1b4c9a) 섹션을 참조하십시오.

## DWB 설치 및 프로비저닝 {#section-424f0ab110434da8a162d212cd22017b}

설치 및 프로비저닝 단계는 클라이언트 워크스테이션과 온-프레미스 서버를 설정하고 특정 요구에 따라 이러한 DWB 구성 요소를 프로비저닝하고 구성하는 데 도움이 됩니다.

자세한 내용은 [설치 및 프로비저닝](../../home/dwb-implement-overview/dwb-implement-provision/dwb-implement-provision.md#concept-a1ec50671ffd4a8faab09a48bc098e8f) 섹션을 참조하십시오.

## DWB 아키텍처 설정 {#section-30d335c856934d56a61790b11bc9b456}

DWB 아키텍처를 사용하여 데이터 피드를 설정하고 스키마를 디자인할 수 있습니다.

자세한 내용은 [아키텍처](../../home/dwb-implement-overview/dwb-implement-architecture/dwb-implement-architecture.md#concept-63dc9aa839e54bc78f7a3d720ce97d56) 섹션을 참조하십시오.

## DWB 관리 설정 {#section-4507b78aff7b497d8e0aeb5c8ac13fe1}

DWB 관리 시 액세스 제어, 오류 및 경고, 서버 업그레이드에 대한 정보입니다.

자세한 내용은 [관리](../../home/dwb-implement-overview/dwb-implement-admin.md#concept-68578dac67314c62a67ddfb4f33458a1) 섹션을 참조하십시오.

## DWB 구성 및 구현 {#section-4643c054ca94473e8e98525b12322b52}

DWB 구성 및 구현에 대한 지침입니다.

자세한 내용은 [구성 및 구현](../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-configure.md#concept-baffe3a57f4649cea7b6eff9a7704dc6) 섹션을 참조하십시오.

## DWB 구현 후 {#section-a0e18d7e7d964eff99692444b80c08b2}

DWB를 설정한 후에는 이러한 기능을 구현할 수 있습니다.

자세한 내용은 [기능 구현](../../home/dwb-implement-overview/dwb-implement-deliver/dwb-implement-deliver.md#concept-9afa96d72a544fb4a3d1eb5be799012c) 섹션을 참조하십시오.
