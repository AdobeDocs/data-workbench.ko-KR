---
description: visual_sciences.dll을 Tomcat java 라이브러리 경로에 추가하기 위한 지침입니다.
title: Java 라이브러리 경로 수정
uuid: 1e1a2704-045a-4b35-aa43-1b5bae91dc32
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Java 라이브러리 경로 수정{#modify-the-java-library-path}

visual_sciences.dll을 Tomcat java 라이브러리 경로에 추가하기 위한 지침입니다.

1. Windows 서버에서 Tomcat 설치 디렉토리로 이동합니다. (Tomcat > bin)
1. bin 폴더에서 Tomcat9w.exe(공용 데몬 서비스 관리자)를 실행합니다.

Java 탭의 Java 옵션에서 새 줄을 추가합니다.

```
-Djava.library.path=C:\Sensor directory
```

C:\Sensor directory is the directory containing the visual_sciences.dll 파일
