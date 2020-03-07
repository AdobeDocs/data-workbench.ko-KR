---
description: DPU 성능을 조정하는 지침
solution: Insight
title: DPU 성능 설정
uuid: e2b87548-7eb3-4f82-a94e-8ec7c3dc27c2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# DPU 성능 설정{#dpu-performance-settings}

DPU 성능을 조정하는 지침

* [!DNL Insight Server] 설치 디렉토리*\Components\DPU.cfg 파일에서 다음 매개 변수를 완료합니다.

| 매개 변수 | 설명 |
|---|---|
| 실행 배치 수 | 조정 매개 변수입니다. 기본값은 65536입니다. 임의 작은 실행 배치 수를 지정할 수 있습니다. 이 값을 변경하기 전에 Adobe에 문의하십시오. |
| 실행 배치 | 조정 매개 변수입니다. 기본값은 128입니다. 이 값을 변경하기 전에 Adobe에 문의하십시오. |
| 실행 시간 | 조정 매개 변수입니다. 기본값은 0.100입니다.이 값을 변경하기 전에 Adobe에 문의하십시오. |
| 오류 시 필드 덤프 | 이 매개 변수는 true 또는 false로 설정할 수 있습니다. true로 설정된 경우 실행 엔진 오류가 발생할 때마다 추적 [!DNL Insight Server] [!DNL Field Dump number.txt] 디렉토리에 이름이 지정된 파일을 만듭니다. &lt; [!DNL Field Dump] > [!DNL number][!DNL .txt] 은 문제 해결에 유용합니다. |
| 프로필 경로 | 모든 프로필의 파일을 저장할 위치입니다. 기본 위치는 Profiles\입니다. |
| 쿼리 메모리 제한 | 쿼리 결과를 저장하는 데 [!DNL Insight Server] 예약된 메모리(바이트)입니다. 기본값은 1000000000(100MB)입니다. 쿼리 결과에 더 많은 공간이 필요한 경우(예: 더 많은 동시 사용자를 허용하기 위해) 설정을 늘릴 수 있지만 [!DNL Insight Server’s] 메모리 로드를 계속 확인해야 합니다. |
| 상태 경로 | 시스템 상태 파일의 위치입니다. 기본 위치는 상태\입니다. |
| 스레드 | 다중 프로세서가 있는 [!DNL Insight Server] 시스템의 성능 조정 매개 변수입니다. 일반적으로 N-코어 시스템의 경우 이 값을 n으로 설정해야 합니다.기본값은 1입니다. |
| 사용자 경로 | 권한이 있는 사용자의 파일 위치입니다. 기본 위치는 사용자\입니다. |

