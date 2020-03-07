---
description: 세그먼트 내보내기 마법사를 사용하여 세그먼트 내보내기
title: 세그먼트 내보내기 마법사
uuid: 705bdf00-54e5-4992-8978-91afda8c7543
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Segment export wizard{#segment-export-wizard}

세그먼트 내보내기 마법사를 사용하여 세그먼트 내보내기

세그먼트 내보내기 마법사는 세부 사항 테이블에서 [세그먼트를](https://docs.adobe.com/content/help/en/data-workbench/using/client/export-data/c-sgmt-expt.html)내보내지 않고 세그먼트를 구성하고 내보내는 단계별 프로세스를 제공합니다.

## 마법사를 사용하여 세그먼트 내보내기 {#section-b30f2699dbc7490bad18512b91cb0cb3}

마법사를 열려면 작업 영역을 마우스 오른쪽 단추로 클릭하고 관리 > 마법사 **> 세그먼트** **** 내보내기 **마법사를**&#x200B;선택합니다.

>[!NOTE]
>
>마법사를 열기 전에 적용된 세그먼트만 캡처됩니다. 또한 마법사에서 생성된 세그먼트 내보내기는 외부 명령을 생성할 수 없습니다.

1. 내보내기에 추가할 차원 및 지표의 다양한 상위 수준을 선택합니다.

   표시되는 수준은 선택한 프로필에 따라 다릅니다. 프로파일을 기반으로 여러 차원 레벨을 선택할 수 있습니다.

   ![](assets/seg_wizard_1.png)

1. **다음**&#x200B;을 클릭합니다.
1. 선택한 수준에 대한 차원 및 지표를 선택합니다.

   예를 들어 페이지 보기를 상위 수준으로 선택한 후 내보낼 수 있는 하위 차원 및 지표를 선택할 수 있습니다.

1. **다음**&#x200B;을 클릭합니다.

   ![](assets/seg_wizard_2.png)

   ![](assets/seg_wizard_2_1.png)

1. 내보내기 형식을 선택하고 내보내기 파일의 이름을 입력합니다.

   ![](assets/seg_wizard_3.png)

   CSV, TSV, 세그먼트 내보내기 및 헤더 유형이 있는 세그먼트 내보내기를 추가로 구성할 필요가 없습니다. 그러나 3단계에서 프로필 및 대상 내보내기, 사용자 지정 레코드 서비스 및 Adobe Target 내보내기를 구성해야 합니다. 예를 들어 프로필 및 대상 내보내기의 구성 필드를 참조하십시오. 이러한 내보내기 유형을 구성하고 다음을 **클릭합니다**.

   ![](assets/seg_wizard_3_1.png)

   ![](assets/seg_wizard_3_2.png)

   ![](assets/seg_wizard_3_3.png)

1. 선택한 내보내기 유형을 구성합니다.

   헤더 - 헤더가 True이면 출력 파일 **필드의 이름을 지정합니다** .

   이스케이프 필드(Escape Field) - **참** 또는 **거짓**(True)으로 설정합니다.

   필드 순서 - 필드를 선택하고 위나 아래로 이동하여 내보내기 파일의 순서를 설정합니다.

   ![](assets/seg_wizard_4.png)

   **다음**&#x200B;을 클릭합니다.

1. 이 대화 상자에서 수준 및 적용된 필터를 봅니다. **다음**&#x200B;을 클릭합니다. ![](assets/seg_wizard_5.png)

1. CSV, **TSV**, ****&#x200B;세그먼트 내보내기 **또는 헤더와 함께** **** 세그먼트 내보내기를 선택한 경우 다음 세 가지 옵션이 있습니다.

   일반 내보내기 - 서버가 서버/내보내기 폴더에 출력 파일을 생성합니다.

   ![](assets/seg_wizard_6.png)

   FTP 내보내기 - 출력 파일이 선택한 서버로 전송됩니다. (서버의 목록은 FTPServerInfo.cfg 파일에서 선택됩니다.)

   ![](assets/seg_wizard_6_1.png)

   SFTP 내보내기 - 출력 파일은 선택한 서버로 안전하게 전송됩니다.

1. **다음**&#x200B;을 클릭합니다

   **참고:** 선택한 내보내기 유형이 **프로필 및 대상 내보내기**, **사용자 지정 레코드 서비스**&#x200B;및 **Adobe Target**&#x200B;내보내기이면선택한 내보내기에 따라 텍스트가 정적으로 표시됩니다.

1. 예약 매개 변수를 구성합니다.

   **한 샷을** True 또는 False로 설정할 수 있습니다.

   **고급 예약** 구성 단추를 클릭하여 고급 예약을 켜거나 끌 수 있습니다.

   ![](assets/seg_wizard_7.png)

   세부 정보 테이블에서 내보내기와 마찬가지로 고급 설정이 켜지면 한 장의 샷이 사라집니다. **다음**&#x200B;을 클릭합니다.

1. 내보내기 파일을 미리 본 다음 내보내기 실행을 **클릭합니다**.

   ![](assets/seg_wizard_8.png)

   ![](assets/seg_wizard_8_1.png)

마법사를 사용하여 다음 내보내기 유형을 사용할 수 있습니다.

**세그먼트 내보내기 유형**

* 범용
* FTP
* SFTP

**헤더와 함께 세그먼트 내보내기**

* 범용
* FTP
* SFTP

**CSV 내보내기**

* 범용
* FTP
* SFTP

**TSV 내보내기**

* 범용
* FTP
* SFTP
