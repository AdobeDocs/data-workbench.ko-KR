---
description: 처리 Insight Server는 구성 요소 디렉토리의 컨텐츠를 제외한 마스터 Insight Server와 동일합니다.
solution: Insight
title: 처리 인사이트 서버 설치 및 구성
uuid: 186675f7-8b63-4675-89ec-51b0837a64d8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 처리 인사이트 서버 설치 및 구성{#installing-and-configuring-the-processing-insight-servers}

처리 Insight Server는 구성 요소 디렉토리의 컨텐츠를 제외한 마스터 Insight Server와 동일합니다.

처리 중인 Components 디렉토리에는 처리를 위해 특별히 구성된 특수 파일 세트가 [!DNL Insight Server] 들어 [!DNL Insight Servers]있습니다. 이러한 파일은 마스터의 처리 서버용 구성 요소 디렉토리에서 파생됩니다 [!DNL Insight Server].

처리를 설치할 [!DNL Insight Server]때 다음을 수행하여 Components 디렉토리를 설정합니다.

1. 처리에서 원본 구성 요소 디렉토리를 삭제합니다 [!DNL Insight Server].
1. 처리 서버 구성 요소 디렉토리의 이름을 구성 요소로 변경합니다.
1. Components [!DNL Synchronize.cfg] 디렉토리에서 마스터를 가리키도록 수정합니다 [!DNL Insight Server].

**처리를 설치 및 구성하려면[!DNL Insight Server]**

1. Insight Server 프로그램 파일 설치에 설명된 [!DNL Insight Server] 대로 프로그램 파일을 설치합니다 [](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088). 마스터에 사용된 디렉토리 구조를 복제해야 [!DNL Insight Server]합니다. 예를 들어, 마스터에 [!DNL Insight Server] 설치되어 [!DNL C:\Adobe\Server] 있는 [!DNL Insight Server]경우 [!DNL C:\Adobe\Server] 처리 과정에도 설치해야 [!DNL Insight Servers] 합니다.
1. Adobe가 이 특정 처리에 대해 발행한 디지털 인증서를 [!DNL Insight Server]설치합니다. 자세한 [내용은 디지털 인증서 다운로드 및](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17) 설치를 참조하십시오.
1. Windows 탐색기를 사용하여 다음 작업을 [!DNL Insight Server]수행하십시오.

   1. Delete the **[!UICONTROL Components]** folder.
   1. 폴더 이름을 구성 요소로 [!DNL Components for Processing Servers] 변경합니다.

1. 메모장과 같은 텍스트 편집기를 사용하여 처리 중인 구성 요소 디렉토리에서 [!DNL Synchronize.cfg] 파일을 엽니다 [!DNL Insight Server].
1. 다음 파일 조각에 표시된 대로 마스터(기본) [!DNL Insight Server] 의 IP 주소를 이 파일의 두 번째 줄에 추가합니다. 이 파일에서 다른 내용은 편집하지 마십시오.

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
1. Insight Server [!DNL Insight Server] 를 Windows 서비스로 등록에 설명된 [대로 시작합니다](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

   이제 [!DNL Insight Server] 클러스터 설치를 완료했습니다. 다음 섹션에 설명된 대로 클러스터에서 실행되도록 데이터 집합 프로필을 구성합니다.

