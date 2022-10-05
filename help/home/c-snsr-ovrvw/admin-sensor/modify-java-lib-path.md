---
description: visual_sciences.dll을 Tomcat java 라이브러리 경로에 추가하는 지침
title: Java 라이브러리 경로 수정
uuid: 1e1a2704-045a-4b35-aa43-1b5bae91dc32
exl-id: bd853d95-3f44-4860-9965-c3210ec4adcf
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 12%

---

# Java 라이브러리 경로 수정{#modify-the-java-library-path}

{{eol}}

visual_sciences.dll을 Tomcat java 라이브러리 경로에 추가하는 지침

1. Windows 서버에서 Tomcat 설치 디렉토리로 이동합니다. (Tomcat > bin)
1. bin 폴더에서 Tomcat9w.exe(일반 데몬 서비스 관리자)를 실행합니다.

Java 탭의 Java 옵션에서 새 줄을 추가합니다.

```
-Djava.library.path=C:\Sensor directory
```

위치 C:\Sensor directory is the directory containing the visual_sciences.dll 파일
