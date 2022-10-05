---
description: DPU 성능을 조정하는 지침입니다.
title: DPU 성능 설정
uuid: e2b87548-7eb3-4f82-a94e-8ec7c3dc27c2
exl-id: 738c3a76-f8b4-4d84-86ee-ce9b99f50dae
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---

# DPU 성능 설정{#dpu-performance-settings}

{{eol}}

DPU 성능을 조정하는 지침입니다.

*에서 다음 매개 변수를 완료하십시오. [!DNL Insight Server] 설치 디렉토리*\Components\DPU.cfg 파일

| 매개 변수 | 설명 |
|---|---|
| 실행 배치 수 | 조정 매개 변수입니다. 기본값은 65536입니다. 임의로 작은 실행 배치 수를 지정할 수 있습니다. 이 값을 변경하기 전에 Adobe에 문의하십시오. |
| 실행 배치 | 조정 매개 변수입니다. 기본값은 128입니다. 이 값을 변경하기 전에 Adobe에 문의하십시오. |
| 실행 시간 | 조정 매개 변수입니다. 기본값은 0.100입니다. 이 값을 변경하기 전에 Adobe에게 문의하십시오. |
| 오류 시 필드 덤프 | 이 매개 변수는 true 또는 false로 설정할 수 있습니다. true로 설정하면 [!DNL Insight Server] 라는 파일을 만듭니다. [!DNL Field Dump number.txt] 실행 엔진 오류가 발생할 때마다 추적 디렉터리에 저장됩니다. 다음 [!DNL Field Dump] &lt; [!DNL number]> [!DNL .txt] 은 문제 해결에 유용합니다. |
| 프로필 경로 | 모든 프로필에 대한 파일을 저장할 위치입니다. 기본 위치는 프로필\ 입니다. |
| 쿼리 메모리 제한 | 해당 메모리 양(바이트) [!DNL Insight Server] 쿼리 결과를 저장할 예약입니다. 기본값은 100000000(100MB)입니다. 쿼리 결과를 위한 공간이 더 필요한 경우(예: 더 많은 동시 사용자를 허용하기 위해) 설정을 늘릴 수 있지만 계속 [!DNL Insight Server’s] 메모리 로드. |
| 상태 경로 | 시스템 상태 파일의 위치입니다. 기본 위치는 상태\ 입니다. |
| 스레드 | 성능 조정 매개변수 [!DNL Insight Server] 여러 프로세서가 장착된 시스템 일반적으로 n-코어 시스템의 경우 이 값을 n으로 설정해야 합니다. 기본값은 1입니다. |
| 사용자 경로 | 권한이 있는 사용자의 파일 위치입니다. 기본 위치는 사용자\입니다. |
