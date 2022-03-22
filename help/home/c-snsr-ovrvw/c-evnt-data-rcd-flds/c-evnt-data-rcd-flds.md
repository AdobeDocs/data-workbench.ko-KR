---
description: 로그(.vsl) 파일에는 센서가 서버에서 수집하고 데이터 집합 구성 프로세스에서 Data Workbench 서버에서 사용하는 이벤트 데이터 필드가 포함되어 있습니다.
title: 이벤트 데이터 레코드 필드(.vsl 파일)
uuid: ad9e773c-a128-4094-9e20-45a6de025c8f
exl-id: d48b593f-5a3a-4a4e-9a71-3b91024c9a48
source-git-commit: 235b8816c7397ac1ab71df650a1d4c2d681b3b2d
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# 이벤트 데이터 레코드 필드{#event-data-record-fields}

로그(.vsl) 파일에는 센서가 서버에서 수집하고 데이터 집합 구성 프로세스에서 Data Workbench 서버에서 사용하는 이벤트 데이터 필드가 포함되어 있습니다.

필드의 이름은 일반적으로 W3C 확장 로그 파일 형식에 대한 이름 지정 규칙을 따릅니다. 많은 필드에 필드에 포함된 정보의 소스를 나타내는 접두사가 있습니다.

* &quot;cs&quot;는 클라이언트로부터 서버로의 통신을 나타냅니다
* &quot;sc&quot;는 서버에서 클라이언트로의 통신을 나타냅니다
* &quot;s&quot;는 서버의 정보를 나타냅니다
* &quot;c&quot;는 클라이언트의 정보를 나타냅니다
* &quot;x&quot;는 Adobe 제품이 만드는 정보를 나타냅니다
