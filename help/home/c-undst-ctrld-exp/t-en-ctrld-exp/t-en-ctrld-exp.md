---
description: 제어 실험을 활성화하려면 웹 또는 응용 프로그램 서버에 대한 관리자 액세스 권한이 있는 사람이 센서가 설치된 웹 클러스터의 각 웹 또는 응용 프로그램 서버에서 Sensor 구성 파일(일반적으로 txlogd.conf를 사용하여 이름)의 ExpFile 매개 변수를 수정해야 합니다.
solution: Analytics
title: 통제 실험 활성화
uuid: 27d68fad-ae2d-4a2e-b449-fbaf88286cfa
exl-id: 53c18524-6050-4708-af63-9e8ef8da389e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# 통제 실험 활성화{#enabling-controlled-experimentation}

{{eol}}

제어 실험을 활성화하려면 웹 또는 응용 프로그램 서버에 대한 관리자 액세스 권한이 있는 사람이 센서가 설치된 웹 클러스터의 각 웹 또는 응용 프로그램 서버에서 Sensor 구성 파일(일반적으로 txlogd.conf를 사용하여 이름)의 ExpFile 매개 변수를 수정해야 합니다.

또한 이 파일에 있는 다른 두 매개 변수를 수정하여 테스트 도구(ExpCookieURL 매개 변수)를 구현하거나 웹 사이트의 큰 섹션(ExpPartialMatch 매개 변수)을 다시 매핑할 수 있습니다. 이 장에서는 이러한 매개 변수에 대한 자세한 정보를 제공합니다.

**txlogd.conf 파일을 편집하려면**

관리자 액세스 권한이 있는 경우 다음 단계를 완료하십시오. 관리자 액세스 권한이 없는 경우 시스템 설계자에게 문의하여 다음 단계를 제공합니다.

1. 로 이동합니다 [!DNL Sensor] 웹 클러스터의 웹 또는 응용 프로그램 서버에 설치 폴더 [!DNL Sensor] 가 설치되어 있습니다.
1. 를 엽니다. [!DNL Sensor] 구성 파일(일반적으로 [!DNL txlogd.conf])에서 텍스트 편집기를 사용하여 에 표시된 대로 파일을 편집합니다 [ExpFile 매개 변수 수정](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28).

   (그리고 선택적으로 [ExpCookieURL 매개 변수 수정(선택 사항)](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expckurl-prm.md#concept-215bf86bab4e4ec0b0cc803ec48a8fcf) 및 [ExpPartialMatch 매개 변수 수정(선택 사항)](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expplmth-prm.md#concept-9c817c4c49b74287b0f70d6a1a37655e))

1. 파일을 저장하고 닫습니다.
1. 웹 클러스터의 각 웹 또는 응용 프로그램 서버에 대해 이 절차를 반복합니다. [!DNL Sensor] 가 설치되어 있습니다.
