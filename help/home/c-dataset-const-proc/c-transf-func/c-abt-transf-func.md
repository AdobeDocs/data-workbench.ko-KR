---
description: 변환 기능(변형)은 데이터 워크벤치 서버 시스템에서 실행되어 다른 응용 프로그램에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.
title: 변환 기능 정보
uuid: f797f283-025b-4fb5-a110-84a9483dccaa
exl-id: db5d6329-407d-43f3-92fc-1b40f7289916
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---

# 변환 기능 정보{#about-transformation-functionality}

변환 기능(변형)은 데이터 워크벤치 서버 시스템에서 실행되어 다른 응용 프로그램에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.

[!DNL Transform] 파일,  [!DNL .vsl] 로그 파일, XML 파일 및 ODBC 데이터를 읽고 데이터를  [!DNL .vsl] 파일, 텍스트 파일 또는 구분된 텍스트 파일로 내보낼 수 있으며 DataWarehouse 로드 루틴, 감사 기관 또는 기타 타겟에서 사용할 수 있습니다. 데이터 추출 및 변환은 연속 또는 기타 예약된 기준으로 수행할 수 있습니다.

>[!NOTE]
>
>일반적으로 [!DNL Transform]은(는) 데이터 워크벤치 서버 FSU에 구성됩니다. 하지만, 구현에 데이터 워크벤치 서버 DPU에 대한 구성이 필요할 수 있습니다. 자세한 내용은 Adobe에 문의하십시오.

자세한 상태 인터페이스에서 [!DNL Transform]의 메모리 사용 정보를 볼 수 있습니다. 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;의 관리 인터페이스 장을 참조하십시오.

세그먼트 내보내기 기능은 Adobe 응용 프로그램에서 데이터를 내보내는 다른 방법을 제공합니다. [!DNL Transform] 처리되지 않은 데이터를 외부 타겟으로 내보낼 수 있지만 세그먼트 내보내기 기능을 사용하면 처리된 데이터를 데이터 세트에서 출력할 수 있으며 내보낸 데이터를 데이터 세트에 차원으로 정의해야 합니다. 세그먼트 내보내기에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.
