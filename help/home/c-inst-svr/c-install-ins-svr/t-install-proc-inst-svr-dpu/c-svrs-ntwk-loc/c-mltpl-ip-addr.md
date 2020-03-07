---
description: '클라이언트가 여러 네트워크를 통해(예: 회사 인트라넷과 인터넷을 통해) Insight Server에 도달할 수 있는 경우 주소 파일은 각 서버의 IP 주소에 대해 별도의 네트워크 위치를 정의해야 합니다.'
solution: Insight
title: Insight 서버에 대한 여러 IP 주소
uuid: 6ed00b47-8ba3-4127-a5db-7e684e573d9c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Insight 서버에 대한 여러 IP 주소{#multiple-ip-addresses-for-an-insight-server}

클라이언트가 여러 네트워크를 통해(예: 회사 인트라넷과 인터넷을 통해) Insight Server에 도달할 수 있는 경우 주소 파일은 각 서버의 IP 주소에 대해 별도의 네트워크 위치를 정의해야 합니다.

예를 들어, 서버에 내부 네트워크에 10.2.1.70 [!DNL VS01.myCompany.com] 의 IP 주소와 인터넷상의 IP 주소 65.196.125.167이 있는 경우 주소 파일에는 아래 예와 같이 각 주소에 대한 네트워크 위치가 포함됩니다.

```
0 = NetworkLocation: 
  Addresses = vector: 1 items
    0 = AddressDefinition: 
      Address = string: 10.2.1.70
      Name = string: VS01.myCompany.com
  Name = string: MyCorporateIntranet
  Parent = string: 
1 = NetworkLocation: 
  Addresses = vector: 1 items
    0 = AddressDefinition: 
      Address = string: 65.196.125.167
      Name = string: VS01.myCompany.com
  Name = string: Internet
  Parent = string:
```

사용자가 NetworkLocation 매개 변수(클라이언트 사용자 인터페이스)를 사용하여 서버의 공통 이름을 확인할 네트워크 위치를 지정합니다. [!DNL Insight Server] 예를 들어, 위에 표시된 두 개의 NetworkLocations가 있는 주소 파일이 있는 경우 사용자는 NetworkLocation 매개 변수를 &quot;MyCorporate Intranet&quot;로 설정하여 내부 네트워크를 [!DNL Insight Server] 통해 연결하고 인터넷을 통해 서버에 연결합니다.
