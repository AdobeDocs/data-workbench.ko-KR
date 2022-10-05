---
description: '클라이언트가 여러 네트워크를 통해(예: 회사 인트라넷 및 인터넷을 통해) Insight Server에 연결할 수 있는 경우 주소 파일은 각 서버의 IP 주소에 대해 별도의 네트워크 위치를 정의해야 합니다.'
title: Insight Server에 대한 여러 IP 주소
uuid: 6ed00b47-8ba3-4127-a5db-7e684e573d9c
exl-id: 71654a60-af82-45f2-826b-29ecc7127b0b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---

# Insight Server에 대한 여러 IP 주소{#multiple-ip-addresses-for-an-insight-server}

{{eol}}

클라이언트가 여러 네트워크를 통해(예: 회사 인트라넷 및 인터넷을 통해) Insight Server에 연결할 수 있는 경우 주소 파일은 각 서버의 IP 주소에 대해 별도의 네트워크 위치를 정의해야 합니다.

예를 들어, 서버가 [!DNL VS01.myCompany.com] 에는 내부 네트워크에 대한 IP 주소가 10.2.1.70이고 인터넷에 있는 IP 주소가 65.196.125.167인 경우 주소 파일에는 아래 예와 같이 각 주소의 네트워크 위치가 포함됩니다.

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

사용자가 [!DNL Insight Server]로 지정하는 경우 클라이언트 사용자 인터페이스에서 NetworkLocation 매개 변수를 사용하여 서버의 일반 이름을 확인할 네트워크 위치를 지정합니다. 예를 들어, 위에 표시된 두 NetworkLocations의 주소 파일이 주어지면 사용자는 NetworkLocation 매개 변수를 &quot;MyCorporate Intranet&quot;로 설정하여 [!DNL Insight Server] 내부 네트워크를 통해 그리고 인터넷을 통해 서버에 연결하기 위해 &quot;인터넷&quot;으로 이동합니다.
