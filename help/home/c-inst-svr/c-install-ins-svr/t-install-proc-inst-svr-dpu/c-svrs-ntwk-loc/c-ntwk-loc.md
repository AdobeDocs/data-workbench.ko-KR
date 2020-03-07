---
description: 개념적으로, 주소 파일은 네트워크 시스템의 ETC\HOSTS 파일과 같은 용도로 사용됩니다.
solution: Insight
title: 네트워크 위치
uuid: a2097eca-dd75-4d43-b8a8-fb4c768df38d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 네트워크 위치{#network-locations}

개념적으로, 주소 파일은 네트워크 시스템의 ETC\HOSTS 파일과 같은 용도로 사용됩니다.

하지만 단일 이름 컬렉션을 설명하는 HOSTS 파일과 달리 주소 파일에는 네트워크 위치라는 이름의 여러 컬렉션이 들어 있습니다.

네트워크 위치는 주소 정의의 명명된 컬렉션입니다. 컬렉션의 각 주소 정의는 공통 이름과 IP 주소를 연결합니다.

주소 파일에서 네트워크 위치는 NetworkLocation이라는 구조에 정의됩니다. 다음 예제의 NetworkLocation은 &quot;MyCorporate Intranet&quot;이라는 네트워크 위치를 정의합니다. 여기에는 공통 이름을 IP 주소 &quot;10.2.1.70&quot; [!DNL VS01.myCompany.com] 에 매핑하는 주소 정의가 포함되어 있습니다.

```
0 = NetworkLocation: 
  Addresses = vector: 1 items
    0 = AddressDefinition: 
      Address = string: 10.2.1.70
      Name = string: VS01.myCompany.com
  Name = string: MyCorporateIntranet
  Parent = string: 
```

위의 예에서 보듯이 NetworkLocation 구조는 다음 세 가지 기본 매개 변수로 구성됩니다.

<table id="table_9142A0EFA15E4C37975E7ACE234F6FDD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> 0개 이상의 AddressDefinitions를 정의합니다. 각 AddressDefinition은 공통 이름을 IP 주소와 연결합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1">  이름  </td> 
   <td colname="col2"> NetworkLocation에 이름을 할당합니다. NetworkLocation에 할당된 이름은 주소 파일 내에서 고유해야 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> <p>이 NetworkLocation에 멤버가 포함된 다른 NetworkLocation의 이름을 지정합니다. 이 매개 변수를 사용하면 한 NetworkLocation이 다른 NetworkLocation을 확장할 수 있습니다. </p> <p>Parent 매개 변수를 "DNS"로 설정하여 NetworkLocation을 클라이언트의 일반 DNS 시스템으로 확장할 수 있습니다. </p> <p>예:상위 = 문자열:DNS </p> <p>DNS가 부모인 경우 클라이언트가 NetworkLocation을 통해 이름을 확인할 수 없을 때 클라이언트 컴퓨터의 DNS 시스템을 사용하여 공통 이름을 확인하려고 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

