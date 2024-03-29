---
description: 웹 사이트 마케팅에는 타사 웹 사이트에서 제공되는 이미지 또는 기타 리치 미디어 파일(웹 서버에서 제공)의 형태로 광고를 배치하는 작업이 포함될 수 있습니다.
title: 광고 노출 측정
uuid: ca2bd6bf-4f49-406c-b47a-18d6abfb48a4
exl-id: 77cd816e-63a4-4080-ac65-0661e1de4ec0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 4%

---

# 광고 노출 측정{#measuring-advertisement-impression}

{{eol}}

웹 사이트 마케팅에는 타사 웹 사이트에서 제공되는 이미지 또는 기타 리치 미디어 파일(웹 서버에서 제공)의 형태로 광고를 배치하는 작업이 포함될 수 있습니다.

이러한 경우 브라우저에서의 광고 노출과 웹사이트의 광고 타겟 URL에 대한 후속 클릭스루(있는 경우)를 모두 측정할 수 있습니다.

이미지 형식의 광고에 대해 다음을 추가합니다 [!DNL Log=1] 쿼리 문자열로 설정하면 이미지 요청이 발생하고 이에 의해 광고 노출이 캡처됩니다. [!DNL Sensor] 를 사용하십시오.

```
<!—REFERENCE IMPRESSION TAG->
<IMG SRC="https://www.mysite.com/images/zag.gif?Log=1&v_ic=CAMPAIGN 1&v_ica=72890ab&v_icr=https://money.cnn.com/markets/"/>
<!--END REFERENCE IMPRESSION TAG-->
```

| 수집한 데이터 | 설명 | 예 |
|---|---|---|
| v_ic= | 노출 캠페인을 나타내는 값 | v_ic=&quot;CAMPAIGN1&quot; |
| v_ica= | 노출 캠페인 자산을 나타내는 값 | v_ica=&quot;72890ab&quot; |
| v_icr= | 노출 캠페인 레퍼러를 나타내는 값 | v_icr=&quot;https://money.cnn.com/markets/ |

추가 외에 [!DNL Log=1] 이미지 요청에는 광고에서 웹 사이트 내의 타겟 페이지로 이동하는 URL에 식별자를 추가하여 클릭스루로 이어진 광고를 추적하고 클릭스루를 해당 광고에 대한 특정 캠페인으로 다시 추적해야 합니다.

```
<a href=”www.mysite.com/path/to/landingpage?Log=1&v_c=CAMPAIGN&v_ca=72890ab&v_cr=https://money.cnn.com/markets/”>
Click Here
</a>
```

<table id="table_B87134C522EF4AC9BD2AFA6F4A0CF574">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 수집한 데이터 </th>
   <th colname="col2" class="entry"> 설명 </th>
   <th colname="col3" class="entry"> 예 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> v_c= </td>
   <td colname="col2"> 클릭스루 캠페인을 나타내는 값 </td>
   <td colname="col3"> v_c="CAMPAIGN1" </td>
  </tr>
  <tr>
   <td colname="col1"> v_ca= </td>
   <td colname="col2"> 클릭스루 캠페인 자산을 나타내는 값 </td>
   <td colname="col3"> v_ca="72890ab" </td>
  </tr>
  <tr>
   <td colname="col1"> v_cr= </td>
   <td colname="col2"> 클릭스루 캠페인 레퍼러를 나타내는 값 </td>
   <td colname="col3"> <p> <span class="filepath"> v_cr="https://money.cnn.com/</span> </p> <p>시장/ </p> </td>
  </tr>
 </tbody>
</table>
