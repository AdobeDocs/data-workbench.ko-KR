---
description: 센서가 통신하는 데이터 워크벤치 서버(대상 서버)를 변경하려면 센서가 설치된 각 웹 서버에서 txlogd.conf 파일을 편집해야 합니다.
solution: Insight
title: 타겟 데이터 워크벤치 서버 변경
uuid: 931d376d-8622-4858-8290-19ce91538570
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 타겟 데이터 워크벤치 서버 변경{#changing-the-target-data-workbench-server}

센서가 통신하는 데이터 워크벤치 서버(대상 서버)를 변경하려면 센서가 설치된 각 웹 서버에서 txlogd.conf 파일을 편집해야 합니다.

**대상으로 변경하려면[!DNL data workbench server]**

1. 원본 대상 서버와 새 대상 서버를 모두 중지합니다.
1. 원본 대상 서버의 최신 [!DNL .vsl] 파일을 새 대상 서버로 복사합니다. 이후 단계에서 새 대상 서버를 다시 시작하면 새 [!DNL Sensor] [!DNL .vsl] [!DNL .vsl] 파일을 만드는 대신 모든 새 데이터가 현재 기존 파일에 추가됩니다. 이렇게 하려면 다음 단계를 완료하십시오.

   1. 원래 대상 서버에서 설치 디렉토리의 [!DNL \Logs] 폴더를 [!DNL data workbench server] 찾습니다.

   1. 폴더에서 최신 [!DNL .vsl] 파일을 복사합니다.
   1. 새 대상 서버에서 [!DNL \Logs] 설치 디렉토리의 [!DNL data workbench server] 폴더를 찾아 [!DNL .vsl] 이 폴더에 파일을 붙여 넣습니다.

1. 설치된 웹 서버 중 하나에서 [!DNL Sensor] 파일을 열고 편집합니다 [!DNL txlogd.conf] . 이렇게 하려면 다음 단계를 완료하십시오.

   1. 설치 디렉토리를 [!DNL Sensor] 찾아 텍스트 편집기에서 [!DNL txlogd.conf] 파일을 엽니다.

   1. ServerAddress 매개 변수를 찾아 새 대상 서버의 주소를 반영하도록 변경합니다.
   1. 파일을 저장하고 닫습니다.

1. 설치된 나머지 모든 웹 서버에 대해 2-3단계를 [!DNL Sensor] 반복합니다.
1. 원본 대상 서버(계속 사용되는 경우)와 새 대상 서버를 다시 시작합니다.
1. 지정한 새 대상 서버에 데이터가 전송되기 시작합니다.
