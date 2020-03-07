---
description: 데이터 집합 구성은 매개 변수가 데이터 집합 구성에 대한 규칙을 제공하는 구성 파일을 편집하는 프로세스입니다.
solution: Analytics
title: 데이터 세트 구성 이해
topic: Data workbench
uuid: 813933d1-f52d-4584-8edd-ce9cd4aed74a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 데이터 세트 구성 이해{#understanding-dataset-configuration}

데이터 집합 구성은 매개 변수가 데이터 집합 구성에 대한 규칙을 제공하는 구성 파일을 편집하는 프로세스입니다.

생성된 데이터 세트는 실제로 데이터 워크벤치 서버 컴퓨터에 저장된 [!DNL temp.db] 파일에 있지만 데이터 세트에 대한 구성 파일은 프로필의 디렉토리 내에 있습니다. 프로필에는 특정 분석 목적으로 데이터 세트(확장 차원 포함)를 구성하는 구성 파일 집합이 포함되어 있습니다. 또한 프로필에는 지표, 파생된 차원, 작업 영역, 보고서 및 시각화와 같은 엔티티의 정의가 포함되어 있으므로 분석가가 데이터 세트와 상호 작용하고 데이터로부터 정보를 얻을 수 있습니다.

편집 중인 데이터 집합 구성 파일의 프로필을 데이터 집합 프로필이라고 합니다. 데이터 집합 프로필은 상속된 여러 프로필을 참조하므로, 분석 요구 사항에 맞게 Adobe 애플리케이션을 구성할 수 있도록 만들고 유지 관리하는 모든 프로필이 될 수 있습니다. 또한 데이터 세트 프로필은 Adobe 애플리케이션과 함께 제공되는 내부 프로필을 참조하여 애플리케이션에서 사용할 수 있는 모든 기능의 기초를 형성할 수 있습니다.

Adobe 애플리케이션에서 사용할 수 있는 다양한 유형의 프로파일에 대한 자세한 내용은 데이터 워크벤치 *사용 안내서를 참조하십시오*.

<!--
c_req_config_files.xml
-->

모든 Adobe 응용 프로그램에 대한 데이터 집합 프로필에는 Insight Server 컴퓨터에 다음 구성 파일이 있어야 합니다.

* **Profile.cfg:** 프로필에 대해 상속된 프로필 및 처리 서버를 나열합니다. 처리 서버는 프로필의 데이터를 처리하는 Insight Server DPU입니다. Insight Server 클러스터를 설치한 경우 단일 프로파일을 실행할 여러 Insight Server 컴퓨터를 지정할 수 있습니다.

   상속된 프로필을 데이터 세트 프로필의 [!DNL Profile.cfg] 파일에 추가하는 방법은 서버 제품 설치 *및 관리 안내서를 참조하십시오*. Insight Server 클러스터 설치 또는 Insight Server 클러스터에서 실행되도록 데이터 집합 프로필을 구성하는 방법에 대한 자세한 내용은 서버 제품 *설치 및 관리 안내서를 참조하십시오*.

* **Dataset\Log Processing.cfg:** 데이터 집합 구성 프로세스의 로그 처리 단계를 제어합니다. 로그 [처리를 참조하십시오](../../home/c-dataset-const-proc/c-dataset-constr.md#concept-8a63892878004dc389c7dad784fcb061). 파일에 대한 자세한 내용은 [!DNL Log Processing.cfg] 로그 처리 구성 [파일을 참조하십시오](../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

* **Dataset\Transformation.cfg:** 데이터 집합 구성 프로세스의 변형 단계를 제어합니다. 변형을 [참조하십시오](../../home/c-dataset-const-proc/c-dataset-constr.md#concept-88f72e0897a744b5bc03df5039264dda). 이 [!DNL Transformation.cfg] 파일은 일반적으로 프로필별 분석을 위해 데이터 세트를 구성합니다. 파일에 대한 자세한 내용은 [!DNL Transformation.cfg] 변형 구성 [파일을 참조하십시오](../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md).

* **데이터 세트에 파일 포함:** 파일에는 데이터 집합 프로필의 [!DNL dataset include] 또는 [!DNL Log Processing.cfg] [!DNL Transformation.cfg] 파일에 포함된 매개 변수의 하위 집합이 포함되어 있지만 상속된 프로필 내에 저장되고 관리됩니다. [!DNL Dataset include] 파일은 기본 데이터 세트 구성 파일을 보완합니다. 자세한 내용은 데이터 세트 포함 [파일을 참조하십시오](../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

Adobe 응용 프로그램을 구현하는 동안 사용자에게 제공된 데이터 세트 프로필에는 데이터 세트 구성 파일 세트가 포함되어 있으므로 이 파일을 열어 편집하고 저장할 수 [!DNL Profile Manager]있습니다.

자세한 내용은 [!DNL Profile Manager]인사이트 *사용 안내서를 참조하십시오*.

<!--
c_addl_config_files.xml
-->

모든 데이터 세트에 대해서는 필요하지 않지만 이러한 파일을 사용하여 데이터 세트 구성 프로세스의 다른 측면을 제어할 수 있습니다.

* **로그 처리 모드.cfg:** 이 [!DNL Log Processing Mode.cfg] 파일을 사용하면 데이터 세트에 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, 데이터 워크벤치 서버가 상태 파일을 저장하는 빈도를 지정할 수 있습니다. 추가 [구성 파일을 참조하십시오](../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* **Server.cfg:** 이 [!DNL Server.cfg] 파일은 데이터 워크벤치 서버에 연결하는 데이터 워크벤치 시스템의 기본 데이터 캐시 크기(바이트)를 지정합니다. 추가 [구성 파일을 참조하십시오](../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* **Transform.cfg 및 Transform Mode.cfg:** 이러한 파일은 Adobe 애플리케이션에서 사용할 데이터 변환 기능에 대한 사용권을 부여받은 경우에만 사용할 수 있습니다. 이 [!DNL Transform.cfg] 파일에는 로그 소스 및 변환 기능을 위한 데이터 변형을 정의하는 매개 변수가 포함되어 있습니다. 정의하는 변형이 소스 데이터를 조작하여 지정한 형식으로 출력합니다. 이 [!DNL Insight Transform Mode.cfg] 파일을 사용하면 데이터 세트에 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, 변환 기능을 실행하는 Insight Server에서 상태 파일을 저장하는 빈도를 지정할 수 있습니다. 변형 [기능을 참조하십시오](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html).

<!--
c_next_steps.xml
-->

특정 데이터 집합 구성 작업에 대한 자세한 내용을 보려면 아래 표를 사용하여 관심 있는 작업을 찾아 읽으십시오.

<table id="table_394CFB5135274545B5DA37952EC6943E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 만약 당신이... </th> 
   <th colname="col2" class="entry"> 자세한 내용은... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>로그 소스 정의 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> 로그 소스 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리 중 데이터 세트에 들어오는 로그 항목 확인 </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 데이터 필터</a> </p> <p> <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> 로그 항목 조건</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>대량의 이벤트 데이터로 추적 ID 분할 사용 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> 키 분할</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Insight Server가 파일 서버 장치로 실행되도록 구성 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중앙 표준화 서버로 실행되도록 Insight Server 구성 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>시간 차원 생성 및 시간 변환에 사용할 표준 시간대 설정 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> 시간대 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe에서 제공하는 내부 프로필에 포함된 데이터 세트 구성 파일을 약간 변경합니다. </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077"> 기존 데이터 세트 편집 포함 파일 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리에서 변환으로 전달할 데이터의 새 필드 지정 </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> 새 데이터 세트 만들기 포함 파일 </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> 로그 처리 데이터 세트에 파일 포함 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>변형 정의 </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> 데이터 변형 </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> 새 데이터 세트 만들기 포함 파일 </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> 변형 데이터 세트에 파일 포함 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>확장 차원 만들기 </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md"> 확장 차원 </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> 새 데이터 세트 만들기 포함 파일 </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> 변형 데이터 세트에 파일 포함 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리 또는 변환 전체에서 사용할 매개 변수 정의 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 데이터 세트에서 매개 변수 정의 포함 파일 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>데이터 세트를 모니터링하거나 관리할 수 있는 인사이트 인터페이스에 대해 알아봅니다. </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-config-int.md#concept-0ea33a52ce234ec8951e7b4430fbc5ab"> 데이터 세트 구성 인터페이스 작업 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Insight의 차원 메뉴에 나타나지 않도록 특정 확장 차원을 숨깁니다. </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-dataset-comp.md#concept-50d9a004736f42f6b0aa7cde0d6148ff"> 데이터 집합 구성 요소 숨기기 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프로필에서 수정할 수 없거나 수정할 수 없는 특정 데이터 집합 구성 파일 재정의 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-dataset-comp.md#concept-50d9a004736f42f6b0aa7cde0d6148ff"> 데이터 집합 구성 요소 숨기기 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>데이터 세트 재처리 </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재처리 및 재변형 </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

