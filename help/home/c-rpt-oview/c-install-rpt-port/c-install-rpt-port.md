---
description: 보고서 포털을 사용하려면 IIS에서 ASP(응용 프로그램 서버 페이지) 집합을 설치하고 구성해야 합니다.
solution: Analytics
title: 보고서 포털 설치
topic: Data workbench
uuid: 6aeb6038-b0b0-48b9-a020-bc9dfd703c43
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 포털 설치{#installing-the-report-portal}

보고서 포털을 사용하려면 IIS에서 ASP(응용 프로그램 서버 페이지) 집합을 설치하고 구성해야 합니다.

**시작하기 전에**

이 장의 절차는 설치 및 구성 방법에 대해 설명합니다 [!DNL Report Portal]. 이러한 절차를 완료하려면 다음 사항이 필요합니다.

* Microsoft IIS가 설치되어 있고 해당 버전을 알고 있습니다.
* 보고서가 표시되는 보고서 세트의 이름을 [!DNL Report Portal]확인합니다.
* 이러한 보고서 세트에 대한 출력을 [!DNL Report Server] 저장하는 디렉토리 위치를 확인합니다. IIS 응용 프로그램 서버에 이 디렉터리에 대한 액세스 권한이 있는지 확인합니다.

>[!NOTE]
>
>* 을 사용하여 보려면 [!DNL Report Portal]보고서는 특정 이름 지정 규칙을 따라야 합니다. 또한 보고서를 저장하는 디렉토리는 지정된 구조를 따라야 합니다. 이러한 요구 사항에 대한 설명은 보고서 [세트가 보고서 포털과 호환되는지 확인...을 참조하십시오.](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706).
   >
   >
* 이제 보고서 포털의 암호는 AES-256비트와 호환됩니다. Report Portal 2.0으로 업그레이드하는 경우 **users.mdb** 데이터베이스에서 암호의 필드 크기 필드를 50에서 150으로 늘립니다. 업데이트된 암호화를 사용하여 암호를 수용하려면 필드 크기를 늘려야 합니다.
>* Report Portal 2.0으로 업그레이드하는 경우 user.mdb 데이터베이스의 암호 **필드에** 대한 필드 크기를 50에서 150으로 늘립니다. 업데이트된 암호화를 사용하여 암호를 수용하려면 필드 크기를 늘려야 합니다.
>* 이제 보고서 포털은 판매 지원을 통해 강력한 해싱 알고리즘을 제공합니다. Report Portal 2.1 **로**&#x200B;업그레이드하는 경우 *데이터베이스에 필드 크기가 20* 자인 [!DNL users.mdb]PasswordSalt라는 새 텍스트 필드를추가합니다. 이 필드는 암호 소금을 저장하는 데 필요합니다.
>



