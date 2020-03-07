---
description: 데이터 세트 생성의 로그 처리 또는 변형 단계 중 적용할 데이터 변형을 정의할 수 있습니다.
solution: Analytics
title: 변형 정의
topic: Data workbench
uuid: 69dd667b-e465-4c1a-a20e-4384e8988cd0
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 변형 정의{#defining-a-transformation}

데이터 세트 생성의 로그 처리 또는 변형 단계 중 적용할 데이터 변형을 정의할 수 있습니다.

>[!NOTE]
>
>Adobe에서는 [!DNL Log Processing] 또는 [!DNL Transformation Dataset Include] [!DNL Log Processing.cfg] [!DNL Transformation.cfg]in이 아닌 파일이나 파일에서 변형을 정의하는 것이 좋습니다.

다음 변형은 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일에서 정의된 경우에만 작동합니다.

* [URII](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-uri-transf/c-appenduri.md#concept-a0df05dd958645bf8219fc7b0b675ee4)첨부
* [CrossRows](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-crossrows.md#concept-fcace08804f54db397ed631cc13ff4f2)
* [조회 행](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-lookuprows.md#concept-4bd9a1f13ee243e592a6a0008053134f)
* [ODBC 데이터 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)
* [세션화](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-sessionize.md#concept-b1af95c8cba34b248f86de883d914bc0)

**변형을 정의하려면**

1. 변환을 정의할 데이터 세트 구성 파일을 [!DNL Profile Manager] 열려면 을 사용합니다.

   * (권장) 데이터 세트에 포함 파일을 열려면 데이터 세트 포함 [파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).
   * 파일을 열려면 로그 처리 [!DNL Log Processing.cfg] 구성 파일 편집을 참조하십시오 [](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5).

   * 파일을 열려면 변환 구성 [!DNL Transformation.cfg] 파일 편집을 참조하십시오 [](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc).

1. 마우스 오른쪽 단추를 **[!UICONTROL Transformations]**&#x200B;클릭한 다음 **[!UICONTROL Add new]** > *&lt;**[!UICONTROL Transformation type]**>*&#x200B;을 클릭합니다.
1. 변환에 적합한 정보를 입력합니다. 변환 유형에 대한 설명과 해당 매개 변수에 대한 자세한 내용은 다음 섹션을 참조하십시오.

   * [표준 변형](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-standard-transf.md#concept-25f4bdbf8fe74c4aaeb2fcd226243886)
   * [URI 변형](../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-uri-transf/c-uri-transf.md#concept-2dfa0ffcd83d4fb69c1f42ad50dea125)
   * [조회 데이터 통합](../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-int-lookup-data.md#concept-08ff70769a464f50ab14299a344f05c7)

1. 구성 파일에서 변환을 정의한 후 파일을 로컬로 저장하고 데이터 워크벤치 서버의 데이터 세트 프로필에 저장합니다.

       변형 정의 및 편집을 위한 팁:
   
   * 데이터 워크벤치 창에서 변환 구성을 편집할 때 바로 가기 키를 사용하여 잘라내기(Ctrl+x), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그), 모두 선택(Ctrl+a)을 비롯한 기본 편집 기능을 사용할 수 있습니다. 또한 단축키를 사용하여 한 구성 파일( [!DNL .cfg])의 텍스트 또는 전체 변형 정의를 복사하여 다른 구성 파일로 붙여넣을 수 있습니다.
   * 정의한 변환의 경우, Comments 매개 변수에 하나 이상의 주석 라인을 추가하여 변형을 자세히 설명하거나 사용에 대한 메모를 추가할 수 있습니다. 데이터 워크벤치를 사용하여 주석을 추가하려면 **[!UICONTROL Comments]** 레이블을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL Comment Line]**&#x200B;을 클릭합니다.

   * A에서 임의의 변환 구성을 열 수 [!DNL Transformation Dependency Map]있습니다. 구성을 연 후 편집하고 변경 내용을 저장할 수 있습니다. 자세한 [!DNL Transformation Dependency Maps]내용은 데이터 집합 [구성 도구를 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

   * 변환의 빈 문자열 출력은 출력 필드의 비어 있지 않은 문자열을 덮어쓸 수 있습니다.

