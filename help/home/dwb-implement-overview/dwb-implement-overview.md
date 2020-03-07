---
description: 데이터 워크벤치 구현 안내서는 구현 관련 온보딩, 계획 및 기술 질문에 대한 참조 역할을 합니다.
title: Adobe Data Workbench 구현
uuid: 2ea3ef17-29d3-4a68-9444-d9682a773942
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Adobe Data Workbench 구현{#implementing-adobe-data-workbench}

데이터 워크벤치 구현 안내서는 구현 관련 온보딩, 계획 및 기술 질문에 대한 참조 역할을 합니다.

Adobe Data Workbench(DWB 파섹)는 Adobe AnalyTICS Premium(AAP)의 구성 요소입니다. 비즈니스 전문가, 데이터 분석가 및 시스템 설계자를 위한 실시간 다차원 지표 분석, 동적 세그멘테이션, 고급 데이터 시각화 및 확장된 분석 기능을 제공하는 강력하고 구성 가능한 시각적 분석 및 보고 애플리케이션입니다. DWB는 모든 데이터 채널과 상호 작용할 수 있는 방법을 분석하여 기업의 비즈니스 목표의 효과를 측정하고, 트렌드를 정의하고, 예측 모델을 생성하여 예측하며, 비즈니스 프로세스를 최적화하여 성과를 향상시킬 수 있도록 합니다. 여러 채널의 데이터를 분석하여 고객 행동을 전체적으로 파악하고 조직 전체에서 실행 가능한 응답을 식별할 수 있습니다.

DWB는 조직의 요구 사항에 맞게 맞춤화된 AAP의 구성 가능한 분석 툴입니다. DWB를 사용하면 모든 유형의 구조화된 데이터를 시각화하고 전체 데이터 세트에 대해 쿼리를 수행할 수 있으므로 방대한 양의 데이터를 실시간으로 사용자 요구에 맞게 구성할 수 있습니다. 그런 다음 필요한 보고서를 생성하고 필요에 따라 전달할 필요가 있는 보고서를 설정하고 예약할 수 있습니다.

DWB는 다음을 제공합니다.

* 멀티채널 실시간 데이터 상관 관계
* 다양한 소스에서 유연한 데이터 수집
* 강력한 고급 데이터 시각화`<discoiqbr>`

데이터 워크벤치 구현에는 다음 단계가 포함됩니다.

1. 데이터 워크벤치에 대한 온보딩 작업
1. 검색 및 요구 사항
1. 설치 및 프로비저닝
1. 아키텍처 설정
1. 관리 설정
1. 구성
1. 구현 후

## DWB 온보딩 {#section-dc2618f7d1a74d7d8fdba163e4101e44}

이러한 온보딩 지침은 컨설팅 서비스 없이 Adobe 관리 서비스를 사용하여 단일 보고서 세트로 데이터 워크벤치를 구현하는 고객을 위한 것입니다. Adobe Data Workbench 및 Analytics Premium을 처음 사용하는 경우 Adobe 온보딩 팀이 첫 번째 연락처가 됩니다. 표준 Adobe Analytics 또는 이전 버전의 DWB에서 업그레이드하는 경우 Adobe 고객 성공 관리자가 연락하여 초기 가입 절차를 시작할 수 있습니다.

자세한 내용은 [DWB](../../home/dwb-implement-overview/dwb-implement-provision/dwb-implement-onboarding.md#concept-e93aba41b26a410f959c5ca7f8e33355) 온보딩 섹션을 참조하십시오.

## DWB 검색 및 요구 사항 {#section-d49b77576f57427598e366c6accfe6f4}

데이터 워크벤치에서 솔루션을 고안하는 데 필요한 질문 및 작업에 대한 입력을 수집합니다.

자세한 내용은 [검색 및](../../home/dwb-implement-overview/dwb-implement-discovery.md#concept-1544d4864e9e437bbd11b1380c1b4c9a) 요구 사항 섹션을 참조하십시오.

## DWB 파섹 설치 및 프로비저닝 {#section-424f0ab110434da8a162d212cd22017b}

설치 및 프로비저닝 단계는 클라이언트 워크스테이션과 온-프레미스 서버를 설정하고 특정 요구 사항에 맞게 이러한 DWB 구성 요소를 제공 및 구성하는 데 도움이 됩니다.

자세한 내용은 [설치 및](../../home/dwb-implement-overview/dwb-implement-provision/dwb-implement-provision.md#concept-a1ec50671ffd4a8faab09a48bc098e8f) 프로비저닝 섹션을 참조하십시오.

## DWB 아키텍처 설정 {#section-30d335c856934d56a61790b11bc9b456}

DWB 아키텍처를 사용하면 데이터 피드를 설정하고 스키마를 디자인할 수 있습니다.

자세한 내용은 [아키텍처](../../home/dwb-implement-overview/dwb-implement-architecture/dwb-implement-architecture.md#concept-63dc9aa839e54bc78f7a3d720ce97d56) 섹션을 참조하십시오.

## DWB 관리 설정 {#section-4507b78aff7b497d8e0aeb5c8ac13fe1}

DWB 관리 시 액세스 제어, 오류 및 경고, 서버 업그레이드에 대한 정보입니다.

자세한 내용은 [관리](../../home/dwb-implement-overview/dwb-implement-admin.md#concept-68578dac67314c62a67ddfb4f33458a1) 섹션을 참조하십시오.

## DWB 구성 및 구현 {#section-4643c054ca94473e8e98525b12322b52}

DWB 구성 및 구현을 위한 지침

자세한 내용은 [구성 및](../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-configure.md#concept-baffe3a57f4649cea7b6eff9a7704dc6) 구현 섹션을 참조하십시오.

## DWB 사후 구현 {#section-a0e18d7e7d964eff99692444b80c08b2}

DWB를 설정한 후 이러한 기능을 구현할 수 있습니다.

자세한 내용은 [기능](../../home/dwb-implement-overview/dwb-implement-deliver/dwb-implement-deliver.md#concept-9afa96d72a544fb4a3d1eb5be799012c) 구현 섹션을 참조하십시오.
