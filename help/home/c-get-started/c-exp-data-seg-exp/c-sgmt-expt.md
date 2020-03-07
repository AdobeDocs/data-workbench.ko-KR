---
description: 데이터 워크벤치 클라이언트의 세부 사항 테이블 시각화에서 세그먼트 내보내기 정의를 쉽게 만들 수 있습니다.
solution: Analytics
title: 세그먼트 내보내기
topic: Data workbench
uuid: 85c8aa72-23fe-424b-9580-6759dc8f8681
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 세그먼트 내보내기{#segment-export}

데이터 워크벤치 클라이언트의 세부 사항 테이블 시각화에서 세그먼트 내보내기 정의를 쉽게 만들 수 있습니다.

또한 외부 프로세스를 사용하여 결합해야 하는 각 DPU에서 부분적인 결과를 생성하는 대신 이러한 결과를 단일 서버에 자동으로 결합할 수 [!DNL Segment Exports] 있습니다. 세그먼트 내보내기 파일을 만들고, 파일에 [!DNL Profile Manager]저장하고, 출력 파일을 원하는 서버에 업로드할 수 있습니다.

**세그먼트 내보내기 서버를 구성하려면**

이 [!DNL Segment Export] 기능은 각 DPU에서 생성된 별도의 출력 파일이 아닌 세그먼트 내보내기 서버에 단일 출력 파일을 만듭니다. 세그먼트 내보내기 서버는 일반적으로 FSU에서 실행되도록 구성됩니다.

의 Dataset\ 디렉토리에서 Workstation [!DNL Profile Manager][!DNL Segment Export.cfg] 을 열고 서버 주소를 지정합니다. (주소는 IP 또는 정규화된 도메인 이름일 수 있습니다.)

![](assets/segment_export_cfg.png)

세그먼트 내보내기 결과를 수신하는 데이터 워크벤치 서버의 IP입니다. 1회 설정입니다. 가 [!DNL Segment Export.cfg] 없으면 내보내기가 실행되지 않습니다.

**내보내기 디렉토리를 구성하려면**

보안을 위해 세그먼트 내보내기 후에 실행되는 실행 파일 또는 배치 파일은 세그먼트 내보내기 서버의 구성 가능한 스크립트\ 디렉토리에 있어야 합니다.

최종 [!DNL .part] 출력은 구성 가능한 내보내기 디렉토리에 있어야 합니다. 실행할 명령이 명령 및 명령 인수에 있습니다. 명령 인수에 있는 %file%의 인스턴스는 출력 파일의 경로로 대체됩니다.

>[!NOTE]
>
>Data Workbench 5.4를 처음 사용하는 경우 \Exports 폴더가 자동으로 생성됩니다. 버전 5.4 이전에 설정된 이전 내보내기 디렉토리에는 각 세그먼트 내보내기의 파일 이름 앞에 내보내기\ 접두사가 필요합니다. 이제 이 접두사를 추가하면 중복됩니다.

1. 대상 [!DNL Communications.cfg] 서버에서 SegmentExportServer를 서버 목록에 [!DNL Segment Exports]추가합니다. (빨간색으로 표시된 예).

   ![](assets/communications_cfg_example.png)

   내보내기 디렉토리:파일 [!DNL .part] 및 출력 위치를 지정합니다. 공유 디렉토리일 수 있습니다.

   스크립트 디렉토리:모든 실행 파일 또는 일괄 처리 파일이 실행되는 디렉토리를 지정합니다.

1. [!DNL Access Control.cfg], 같은 서버에서 URI /SegmentExportServer/에 대한 읽기-쓰기 액세스 권한을 클러스터 서버 액세스 그룹에 추가합니다.

   ![](assets/accesscontrol_cfg_example.png)

1. 파일 [!DNL .export] 변경:

   ![](assets/segment_export_query_example.png)

1. 각 프로필의 경우 [!DNL Segment Export.cfg] 는 Dataset\ 디렉토리에 있으며 다음 컨텐츠가 있습니다.

   ```
   Segment Export = SegmentExport:
   Segment Export Server = serverInfo:
   Port = int: 80
   Address = string: 192.168.5.128 (for example) Use SSL = bool: false
   ```

1. 내보내기 디렉토리 및 스크립트 디렉토리에 참조된 디렉토리가 있는지 확인합니다.

   Scripts 디렉토리의 실행 파일 및 배치 파일만 세그먼트 내보내기 명령으로 실행할 수 있습니다.

**세그먼트 내보내기 파일을 만들려면**

1. 작업 영역에서 데이터 하위 세트(시각화 > 세부 사항 테이블)를 보여주는 세부 사항 테이블을 만들고 속성을 추가합니다.
1. 원하는 경우 작업 영역에서 선택합니다. 선택 사항이나 필터가 내보내기에 적용됩니다.

   ![](assets/create_segment_export_file.png)

1. 세부 사항 테이블 헤더에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Create Segment Export File]**&#x200B;선택합니다.
1. 에서 [!DNL Save as]파일의 이름을 입력합니다 [!DNL .export] .
1. 파일에서 필요에 따라 매개 변수를 [!DNL .export] 구성합니다.

   작업 영역의 선택 사항이나 필터는 내보내기 파일에 통합됩니다.

1. Save the [!DNL .export] file.

   서버에 저장할 수 [!DNL Profile Manager] 있도록 저장된 파일이 에 표시됩니다. 파일을 서버에 저장하면 내보내기가 시작됩니다.
