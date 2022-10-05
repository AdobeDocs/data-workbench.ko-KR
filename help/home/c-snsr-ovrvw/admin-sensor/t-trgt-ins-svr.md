---
description: 센서가 통신하는 Data Workbench 서버(대상 서버)를 변경하려면 센서가 설치된 각 웹 서버에서 txlogd.conf 파일을 편집해야 합니다.
title: Target Data Workbench 서버 변경
uuid: 931d376d-8622-4858-8290-19ce91538570
exl-id: 9d18cae1-4037-48c6-8514-3278e2c73b47
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 4%

---

# Target Data Workbench 서버 변경{#changing-the-target-data-workbench-server}

{{eol}}

센서가 통신하는 Data Workbench 서버(대상 서버)를 변경하려면 센서가 설치된 각 웹 서버에서 txlogd.conf 파일을 편집해야 합니다.

**target으로 변경하려면[!DNL data workbench server]**

1. 원본 대상 서버와 새 대상 서버를 모두 중지합니다.
1. 가장 최신 복사 [!DNL .vsl] 파일을 원래 타겟 서버에서 새 타겟 서버로 전송합니다. 이후 단계에서 새 대상 서버를 다시 시작하면 모든 새 대상 서버가 생성됩니다 [!DNL Sensor] 현재 기존 데이터에 추가할 데이터 [!DNL .vsl] 새 파일을 만드는 대신 [!DNL .vsl] 파일. 이렇게 하려면 다음 단계를 완료하십시오.

   1. 원래 대상 서버에서 [!DNL \Logs] 폴더의 [!DNL data workbench server] 설치 디렉토리.

   1. 가장 최신 복사 [!DNL .vsl] 파일로 내보낼 때 시간별 세부기간이 작동하지 않는 문제를 해결했습니다.
   1. 새 대상 서버에서 [!DNL \Logs] 폴더의 [!DNL data workbench server] 설치 디렉토리 및 붙여넣기 [!DNL .vsl] 파일을 이 폴더에 추가합니다.

1. 웹 서버 중 하나에서 [!DNL Sensor] 이(가) 설치되면 열고 편집합니다 [!DNL txlogd.conf] 파일. 이렇게 하려면 다음 단계를 완료하십시오.

   1. 다음 위치로 이동합니다. [!DNL Sensor] 설치 디렉토리 및 열기 [!DNL txlogd.conf] 파일을 텍스트 편집기에 저장합니다.

   1. ServerAddress 매개 변수를 찾아 새 대상 서버의 주소를 반영하도록 변경합니다.
   1. 파일을 저장하고 닫습니다.

1. 나머지 웹 서버에서는 2-3단계를 반복합니다 [!DNL Sensor] 가 설치되어 있습니다.
1. 원래 대상 서버(계속 사용 중인 경우)와 새 대상 서버를 다시 시작합니다.
1. 지정한 새 대상 서버로 데이터가 전송되기 시작합니다.
