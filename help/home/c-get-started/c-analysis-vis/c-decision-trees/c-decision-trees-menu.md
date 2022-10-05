---
description: 의사 결정 트리 메뉴에는 긍정적인 사용 사례, 필터, 리프 배포 옵션, 혼동 매트릭스 및 기타 고급 옵션을 설정하는 기능이 포함되어 있습니다.
title: 의사 결정 트리 옵션
uuid: 6439c6d4-60ac-4324-b870-b452a63b7ba1
exl-id: e139562d-4613-4159-a858-2a78a2e896dd
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 2%

---

# 의사 결정 트리 옵션{#decision-tree-options}

{{eol}}

의사 결정 트리 메뉴에는 긍정적인 사용 사례, 필터, 리프 배포 옵션, 혼동 매트릭스 및 기타 고급 옵션을 설정하는 기능이 포함되어 있습니다.

<table id="table_0CBCCB0856E2469EBE8846B413CAB114"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 도구 모음 단추 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이동 </td> 
   <td colname="col2"> 의사 결정 트리 알고리즘을 실행하고 시각화를 표시하려면 을(를) 클릭합니다. 입력이 나올 때까지 회색으로 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재설정 </td> 
   <td colname="col2"> 입력 및 의사 결정 트리 모델을 지우고 프로세스를 재설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 저장 </td> 
   <td colname="col2"><b>의사 결정 트리 저장</b>. 의사 결정 트리를 다른 형식으로 저장할 수 있습니다. 
    <ul id="ul_F7C7836C06D64912893113E8EEA05704"> 
     <li id="li_D2D8451A679243F1BC67C3B80CA5F83F">Predictive Markup Language (<b>PMML</b>). 응용 프로그램에서 의사 결정 트리 모델을 설명하고 교환하기 위해 사용하는 XML 기반 파일 형식입니다. </li> 
     <li id="li_88C4B3E050CA4EFC9B7FA8BD446A9C55"><b>텍스트</b> true 또는 false의 단순 열 및 행, 백분율, 멤버 수 및 입력 값 표시 </li> 
     <li id="li_3F871B88F3FA41E9B95EFF5A181E3D57">A <b>Dimension</b> 예측된 결과 요소에 해당하는 분기 포함. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 옵션 </td> 
   <td colname="col2"> 옵션 메뉴에 대해서는 아래 표를 참조하십시오. </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_24D84440D0354C70928E8927624DB255"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 옵션 메뉴 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 양수 사례 설정 </td> 
   <td colname="col2"> 현재 작업 영역 선택을 모델의 양의 대소문자를 정의합니다. 선택 항목이 없으면 대소문자를 지웁니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 채우기 필터 설정 </td> 
   <td colname="col2"> 현재 작업 공간 선택을 모델의 모집단 필터로 정의하고 이 조건을 충족하는 방문자로부터 그립니다. 기본값은 "모든 사용자"입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 복잡한 필터 설명 표시 </td> 
   <td colname="col2"> 정의된 필터에 대한 설명을 표시합니다. 양수 사례 및 모집단 필터에 대한 필터링 스크립트를 보려면 을 클릭합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 노드 숨기기 </td> 
   <td colname="col2"> 모집단의 소수 백분율만 있는 노드를 숨깁니다. 이 메뉴 명령은 의사 결정 트리가 표시되는 경우에만 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 혼동 매트릭스 </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 옵션</span> &gt; <span class="uicontrol"> 혼동 매트릭스</span> 정확도, 회수, 정밀도 및 F 스코어 값을 보려면 100%에 가까울수록 점수가 높아집니다. </p> <p>혼동 매트릭스는 값 조합을 사용하여 모델의 네 가지 정확도 카운트를 제공합니다. 
     <ul id="ul_D9D512F5D74B44BDBD27B1912DF4CB02"> 
      <li id="li_28C541DF1CB543FEAF2D13C2F329DB52">실제 양수(AP) </li> 
      <li id="li_56233006A1544D95A72CE096CA55C1E6">예측된 양수(PP) </li> 
      <li id="li_375FB2D6A0A3418A9AD377C9EBB65386">실제 음수(AN) </li> 
      <li id="li_07A5D23A36BA4D448C25C1414836EB8E">예상 음수(PN) </li> 
     </ul> </p> <p>팁: 이 숫자들은 보류된 20% 테스트 데이터의 결과 점수 모델을 적용하여 얻으며 이미 정답으로 알려져 있다. 점수가 50%를 초과하는 경우 정의된 필터와 일치하는 긍정적인 대/소문자로 예측됩니다. 그런 다음 정확도 = (TP + TN)/(TP + FP + TN + FN), Recall = TP / (TP + FN) 및 Precision = TP / (TP + FP). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 범례 표시 </td> 
   <td colname="col2">의사 결정 트리에서 범례 키를 켜거나 끌 수 있도록 해줍니다. <img placement="break" id="image_D5B9415A48C04619955BD96970F720A1" src="assets/decison_tree_legend.png" />이 메뉴 명령은 의사 결정 트리가 표시되는 경우에만 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 고급 </td> 
   <td colname="col2"> 의사 결정 트리를 심층적으로 사용하려면 고급 메뉴를 클릭하여 엽니다. 메뉴 옵션에 대해서는 아래 표를 참조하십시오. </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_91E4A74BFB224ABD889147324AC2910F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 고급 메뉴 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 교육 집합 크기 </td> 
   <td colname="col2"> <p>모델 빌드에 사용되는 교육 세트의 크기를 제어합니다. 더 큰 세트는 훈련하는데 더 오래 걸리고, 더 작은 세트는 시간이 적게 걸립니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 표준화 </td> 
   <td colname="col2"> <p> 사용자가 Min-Max 또는 Z 점수 기법을 사용하여 입력사항을 모델에 정규화할지 여부를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 삼투압 과샘플링 요소 </td> 
   <td colname="col2"> 교육 샘플에서 Positive Case 가 매우 자주(10% 미만) 발생하지 않는 경우 SMOTE를 사용하여 추가 샘플을 제공합니다. 이 옵션을 사용하면 SMOTE를 사용하여 만들 샘플 수를 추가로 표시할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 리프 클래스 배포 임계값 </td> 
   <td colname="col2"> 트리 작성 프로세스 중에 리프에 대해 가정된 임계값을 설정할 수 있습니다. 기본적으로 노드의 모든 멤버는 동일해야 합니다. 이 경우 노드가 리프(정리 단계 전)가 됩니다. </td> 
  </tr> 
 </tbody> 
</table>
