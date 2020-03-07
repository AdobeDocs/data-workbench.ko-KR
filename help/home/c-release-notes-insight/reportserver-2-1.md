---
description: 데이터 워크벤치 보고서 포털에 대한 보안 업데이트.
title: DWB Report Portal 2.1
uuid: de8266f4-1f7b-4bfd-94e7-16bddb336db3
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# DWB Report Portal 2.1{#dwb-report-portal}

데이터 워크벤치 보고서 포털에 대한 보안 업데이트.

**중요 보안 업데이트**

이제 보고서 포털은 판매 지원을 통해 강력한 해싱 알고리즘을 제공합니다. Report Portal 2.1로 업그레이드하는 경우 user.mdb 데이터베이스에 20자 필드 크기의 PasswordSalt라는 새 텍스트 필드를 추가합니다. 이 필드는 암호 소금을 저장하는 데 필요합니다.
