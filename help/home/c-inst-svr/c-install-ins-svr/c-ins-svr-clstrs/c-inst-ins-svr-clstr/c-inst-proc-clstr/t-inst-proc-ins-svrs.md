---
description: 처리 Insight 서버는 구성 요소 디렉토리의 컨텐츠를 제외한 마스터 Insight Server와 동일합니다.
title: 처리 Insight Server 설치 및 구성
uuid: 186675f7-8b63-4675-89ec-51b0837a64d8
exl-id: 21f7e31b-a2fb-4257-972e-5228bb1efa01
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 5%

---

# 처리 Insight Server 설치 및 구성{#installing-and-configuring-the-processing-insight-servers}

처리 Insight 서버는 구성 요소 디렉토리의 컨텐츠를 제외한 마스터 Insight Server와 동일합니다.

처리 중인 Components 디렉토리에는 [!DNL Insight Server]의 처리를 위해 특별히 구성된 특수 파일 세트가 포함되어 있습니다. [!DNL Insight Servers] 이러한 파일은 마스터 [!DNL Insight Server]의 처리 서버용 구성 요소 디렉토리에서 파생됩니다.

처리 [!DNL Insight Server]을(를) 설치할 때 다음을 수행하여 해당 Components 디렉토리를 설정합니다.

1. 처리 중인 [!DNL Insight Server]에서 원래 구성 요소 디렉토리를 삭제합니다.
1. 처리 서버용 구성 요소 디렉토리를 구성 요소로 이름을 변경합니다.
1. 마스터 [!DNL Insight Server]을 가리키도록 구성 요소 디렉토리에서 [!DNL Synchronize.cfg]을 수정합니다.

**처리를 설치하고 구성하려면[!DNL Insight Server]**

1. [Insight 서버 프로그램 파일 설치](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088)에 설명된 대로 [!DNL Insight Server] 프로그램 파일을 설치합니다. 마스터 [!DNL Insight Server]에 사용된 디렉토리 구조를 복제해야 합니다. 예를 들어 [!DNL Insight Server]이(가) 마스터 [!DNL Insight Server]의 [!DNL C:\Adobe\Server]에 설치된 경우 처리 [!DNL Insight Servers]의 [!DNL C:\Adobe\Server]에도 설치해야 합니다.
1. 이 특정 처리 [!DNL Insight Server]에 대해 Adobe이 발행한 디지털 인증서를 설치합니다. 지침은 [디지털 인증서 다운로드 및 설치](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17)를 참조하십시오.
1. Windows 탐색기를 사용하여 [!DNL Insight Server] 처리에서 다음을 수행합니다.

   1. **[!UICONTROL Components]** 폴더를 삭제합니다.
   1. [!DNL Components for Processing Servers] 폴더의 이름을 구성 요소로 변경합니다.

1. 메모장과 같은 텍스트 편집기를 사용하여 [!DNL Insight Server] 처리 중인 구성 요소 디렉토리에서 [!DNL Synchronize.cfg] 파일을 엽니다.
1. 다음 파일 조각에 표시된 대로 마스터(기본) [!DNL Insight Server]의 IP 주소를 이 파일의 두 번째 행에 추가합니다. 이 파일의 다른 부분은 편집하지 마십시오.

   ```
   component = SynchronizeComponent:
     Cluster Primary Server Address = string: PrimaryIPAddress
     Directories = vector: 7 items
       0 = SynchronizeDir:
         Local Path = string: Profiles\\
         Remote URI = string: /Profiles/
       1 = SynchronizeDir:
         Local Path = string: Lookups\\
         Remote URI = string: /Lookups/
       . . .
   ```

1. 파일을 저장합니다.
1. [Insight Server를 Windows 서비스](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)로 등록에 설명된 대로 [!DNL Insight Server]을 시작합니다.

   이제 [!DNL Insight Server] 클러스터 설치를 완료했습니다. 다음으로 다음 섹션에 설명된 대로 클러스터에서 실행할 데이터 집합 프로필을 구성합니다.
