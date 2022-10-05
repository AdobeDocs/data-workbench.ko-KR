---
description: Insight Server에 설치된 주소 파일에는 사전 정의된 네트워크 위치가 4개 있습니다.
title: Insight Server에 설치된 주소 파일
uuid: a58d36d8-e1a3-43e7-91c5-c57351e1be49
exl-id: 12e9bfa2-99ac-4584-b761-38401d1bc3d1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 2%

---

# Insight Server에 설치된 주소 파일{#the-address-file-installed-on-insight-server}

{{eol}}

Insight Server에 설치된 주소 파일에는 사전 정의된 네트워크 위치가 4개 있습니다.

다음 섹션의 절차는 이 파일을 구성하는 방법에 대해 설명합니다.

```
Locations = vector: 4 items  
  0 = NetworkLocation:  
    Addresses = vector: 1 items 
      0 = AddressDefinition:  
        Address = string:  
        Name = string:  
    Name = string:  
    Parent = string:  
  1 = NetworkLocation:  
    Addresses = vector: 0 items 
    Name = string: Insight 
    Parent = string:  
  2 = NetworkLocation:  
    Addresses = vector: 0 items 
    Name = string: Insight Server 
    Parent = string: 
  3 = NetworkLocation:  
    Addresses = vector: 0 items 
    Name = string: Report Server 
    Parent = string:
```

* NetworkLocation 0은 사용자의 공통 이름을 연결하기 위해 편집하는 비어 있는 명명되지 않은 네트워크 위치입니다 [!DNL Insight Server] IP 주소로 이동합니다. 서버에 여러 IP 주소가 있는 경우 추가 NetworkLocations를 만듭니다.
* NetworkLocation 1은 [!DNL Insight] 네트워크 위치. NetworkLocation 매개 변수를 명시적으로 설정하지 않으면 [!DNL Insight] 이 네트워크 위치를 통해 일반 이름을 확인합니다.

* NetworkLocation 2는 [!DNL Insight Server] 네트워크 위치. When [!DNL Insight Servers] 클러스터에서 작동하면 이 네트워크 위치를 사용하여 서버 간 통신에 대한 일반 이름을 확인합니다.

* NetworkLocation 3은 [!DNL Report] 서버 네트워크 위치입니다. NetworkLocation 매개 변수를 명시적으로 설정하지 않으면 [!DNL Report] 이 네트워크 위치를 통해 일반 이름을 확인합니다.

## 주소 파일을 구성하려면 {#section-10caab9854a244e39b09071946f7bd27}

다음 절차에서는 주소 파일을 구성하여 사용자의 네트워크 위치(또는 네트워크 위치)를 정의하는 방법에 대해 설명합니다 [!DNL Insight Server].

1. 로 이동합니다 [!DNL Addresses] 설치한 디렉토리의 폴더 [!DNL Insight Server] (예: [!DNL C:\Adobe\Server\Addresses)].

1. 을(를) 찾습니다 [!DNL server.address] 서버의 일반 이름을 반영하도록 이 파일의 이름을 바꾸십시오. 예를 들어, 공통 이름이 [!DNL server.mycompany.com]로 지정하는 경우 파일의 이름을 바꿉니다 [!DNL server.mycompany.com.address].

1. 이름이 변경된 파일을 메모장과 같은 텍스트 편집기에서 엽니다.
1. NetworkLocation 0을 편집하여 [!DNL Insight Server] 아래와 같이 표시됩니다. 서버에 여러 개의 IP 주소가 있는 경우 NetworkLocation 0을 사용하여 라우트할 수 없는 로컬 네트워크에서 서버의 IP 주소를 지정합니다(예: 내부 네트워크상의 위치).

   ```
   Locations = vector: 3 items 
   0 = NetworkLocation: 
     Addresses = vector: 1 items 
       0 = AddressDefinition: 
         Address = string: IPAddress 
         Name = string: CommonName 
     Name = string: NetworkLocationName 
     Parent = string: 
   ```

<table id="table_02C2A1630CCD40C4A51B314C3CB683F1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 값의 경우... </th> 
   <th colname="col2" class="entry"> 분류에 사용할 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>IP 주소</i> </td> 
   <td colname="col2"> <p>의 숫자 IP 주소입니다 <span class="keyword"> Insight Server </span> 시스템. </p> <p>예: 192.168.124.176 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>일반 이름 </i> </td> 
   <td colname="col2"> <p>에 대한 디지털 인증서에 할당된 공통 이름 <span class="keyword"> Insight Server </span>. </p> <p>예: <span class="filepath"> server.mycompany.com </span></p> <p>참고: 이 이름은 인증서에 표시되는 대로 입력해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>네트워크 위치 이름 </i> </td> 
   <td colname="col2"> <p>이 NetworkLocation이 나타내는 공통 이름 및 IP 주소 컬렉션에 할당할 이름입니다. 주소 파일 내에서 이름은 고유해야 합니다. </p> <p>예: 회사 인트라넷 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 만약 [!DNL Insight Server] 에는 추가 IP 주소가 있으며 각 주소에 대해 추가 NetworkLocation을 만듭니다. (위에서 만든 NetworkLocation의 복사본을 만들고 복사본에서 IP 주소를 업데이트하는 것이 간편한 방법입니다.)

   주소 파일의 끝에 새 NetworkLocation을 추가하거나 기존 NetworkLocation 정의 사이에 삽입할 수 있습니다. 주소 파일 내의 NetworkLocation의 위치는 중요하지 않습니다. 하지만, [!DNL Insight], [!DNL Insight Server], 및 [!DNL Report] Server NetworkLocations는 일반적으로 파일의 끝에 배치됩니다.)

   필요한 NetworkLocations를 추가한 후 다음을 수행하여 파일의 항목을 다시 작성합니다.

   1. 파일의 총 NetworkLocation 정의 수와 일치하도록 위치 구조의 항목 수를 업데이트합니다. 예를 들어 파일에 NetworkLocation 정의가 4개 포함되어 있으면 위치 라인은 다음과 같습니다.

      ```
      Locations = vector: 4 items
      ```

   1. NetworkLocations가 연속적으로(0부터 시작)되도록 NetworkLocation 항목 번호를 업데이트합니다.
   다음을 정의하는 주소 파일의 예 [!DNL Insight Server] 두 개의 IP 주소를 사용하는 경우 이 섹션의 예를 참조하십시오.

1. 에서 [!DNL Insight] 및 [!DNL Report] 서버 네트워크 위치, 아래와 같이 Parent 매개 변수를 편집하여 NetworkLocation의 이름을 지정합니다 [!DNL Insight] 및 [!DNL Report] 을 기본 네트워크 위치로 사용합니다. (Parent 매개 변수가 구성되었을 때 나타나는 예와 관련된 예는 이 섹션의 예를 참조하십시오.)

   ```
   1 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Insight 
     Parent = string: ClientDefaultNetworkLocation 
   
   3 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Report Server 
     Parent = string: ClientDefaultNetworkLocation
   ```

   만약 [!DNL Insight Server] 에는 단일 IP 주소가 있으므로 NetworkLocation이 하나만 있으므로 Parent 매개 변수를 해당 NetworkLocation을 가리킵니다. 만약 [!DNL Insight Server] IP 주소가 여러 개 있는 경우 Parent 매개 변수를 NetworkLocation으로 지정하여 [!DNL Insight] 및 [!DNL Report] 클라이언트가 가장 자주 연결합니다.

1. 에서 [!DNL Insight Server] 네트워크 위치에서, 서버가 다른 네트워크 이름을 확인하는 데 사용하는 NetworkLocation을 가리키려면 아래 표시된 대로 Parent 매개 변수를 편집합니다 [!DNL Insight Servers] 클러스터에서 작동하는 경우입니다. ( 이 네트워크 위치는 [!DNL Insight Server] 는 클러스터에서 작동하므로, 단일 서버 구성에서도 서버의 내부 IP 주소를 식별하는 네트워크 위치에 상위 매개 변수를 지정하는 것이 좋습니다.)

   ```
   2 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Insight Server 
     Parent = string: ServerDefaultNetworkLocation
   ```

다음 예는 완성된 주소 파일을 보여줍니다. 이 파일은 5개의 네트워크 위치를 정의합니다.

* NetworkLocation 항목 0 및 1은 &quot;MyCorporateIntranet&quot; 및 &quot;Internet&quot;이라는 네트워크 위치를 정의합니다. 이러한 네트워크 위치는 이름이 인 서버에 대해 두 개의 서로 다른 IP 주소를 정의합니다 [!DNL VS01.myCompany.com].
* NetworkLocation 항목 2는 [!DNL Insight] 네트워크 위치. 이 위치는 [!DNL Insight]. 이 예에서 [!DNL Insight] 네트워크 위치는 &quot;Internet&quot; NetworkLocation에서 해당 AddressDefinitions를 상속합니다.

* NetworkLocation 항목 3은 [!DNL Insight Server] 네트워크 위치. 기본 네트워크 위치입니다 [!DNL Insight Server] 는 클러스터의 다른 서버와 통신할 때 사용합니다. 이 예에서 [!DNL Insight Server] 네트워크 위치는 &quot;MyCorporate&quot; NetworkLocation에서 해당 AddressDefinitions를 상속합니다.

* NetworkLocation 항목 4는 [!DNL Report] 서버 네트워크 위치입니다. 이 위치는 [!DNL Report]. 이 예에서 [!DNL Report] 서버 네트워크 위치는 &quot;인터넷&quot; NetworkLocation에서 해당 AddressDefinitions를 상속합니다.

   ```
   Locations = vector: 5 items 
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
   
     2 = NetworkLocation:  
       Addresses = vector: 0 items 
       Name = string: Insight 
       Parent = string: Internet 
   
     3 = NetworkLocation:  
       Addresses = vector: 0 items 
       Name = string: Insight Server 
       Parent = string: MyCorporateIntranet 
   
     4 = NetworkLocation:  
       Addresses = vector: 0 items 
       Name = string: Report Server 
       Parent = string: Internet
   ```
