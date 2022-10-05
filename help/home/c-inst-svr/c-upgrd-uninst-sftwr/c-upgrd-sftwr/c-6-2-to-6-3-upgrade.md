---
description: Data Workbench 6.3용 서버 구성 요소를 업그레이드하는 중.
title: DWB 서버 6.2에서 6.3으로 업그레이드
uuid: e12b6cc1-070e-4bc7-bc64-203d11cfeae9
exl-id: 5106d9a3-179a-49f1-915a-c03b36ed5257
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 2%

---

# DWB 서버 업그레이드: 6.2에서 6.3으로{#dwb-server-upgrade-to}

{{eol}}

Data Workbench 6.3용 서버 구성 요소를 업그레이드하는 중.

**서버 업그레이드**

에 제공된 기본 파일보다 우선하는 프로필을 사용자 정의한 경우 [!DNL Base] 패키지 를 업데이트한 후 다음 사용자 지정 파일을 업데이트해야 합니다.

* **Meta.cfg 파일 업데이트** ( [!DNL E:\..\Profiles\<your custom profile>\Context\meta.cfg)]파일 시스템 단위(FSU 서버)에 대해 업데이트된 암호 암호화를 설정하고 이름 값 쌍 변환에 대한 항목을 추가하여 [쿼리 문자열 그룹화](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-2-to-6-3-upgrade.md#concept-42f74911b5714219a359b719badac8e0).

   1. 를 엽니다. [!DNL meta.cfg] 파일을 FSU에 저장합니다.
   1. 의 데이터 유형 변경 **[!UICONTROL Proxy Password]** 다음: [!DNL string"] 다음을 수행합니다. [!DNL EncryptedString]&quot; *워크스테이션 구성* 섹션을 참조하십시오.

      ```
        Proxy User Name = string:
        Proxy Password = EncryptedString:   (
        from Proxy Password = String)
        Use Address File = bool: true
      ```

   1. 새 항목을 추가하여 새 이름 값 쌍 변환을 활성화합니다. *BuildNameValuePair* 및 *ExtractNameValuePairs*.

      작업 공간을 열고 마우스 오른쪽 단추 클릭 **관리** > **프로필 관리자**.

      아래 **컨텍스트**&#x200B;를 클릭하고 **meta.cfg** 파일의 **기본** 열을 누른 다음 **로컬 만들기**. 사용자 테이블 열에서 마우스 오른쪽 버튼을 클릭하고 을 선택합니다 **열기** > **워크스테이션**.

      ![](assets/meta_cfg.png)

      * 새 창에서 **메타데이터** 및 허용 가능한 하위 템플릿을 추가합니다.

         ![](assets/meta_cfg_child.png)

      * 열기 **변환** 새 템플릿을 추가합니다.

         ![](assets/meta_cfg_template.png)

* **빠른 병합 개선 사항을 위한 업데이트**. 변환 중 Data Workbench 속도 개선 기능을 활용하기 위해 다음 구성 파일에 매개 변수를 추가하거나 값을 변경합니다.

   * **Communications.cfg** ( [!DNL E:\Server\Components\Communications.cfg])

      ```
      18 = SourceListServer:
          URI = string: /SourceListServer/
          Listing Interval = int: 10 (
      <new>)
      ```

   * **Disk Files.cfg** (at) [!DNL E:\Server\Components] 및 [!DNL E:\Server\Components for Processing Servers])

      ```
      Disk Cache Size (MB) = double: 1024
      <(from double: 256)>
      Disk Cache Read Limit (MB) = double: 768
      <(new)>
      ```

   * **Log Processing Mode.cfg** ( [!DNL E:\Server\Profiles\<your profile>\Dataset\Log Processing Mode.cfg])

      ```
      <(changed)
      Batch Bytes = int: 268435456
      Cloud Bytes = int: 268435456
      Real Time FIFO Bytes = int: 268435456
      ```

      ```
      (
      <new>)
      Cache Bytes = int: 32000000
      Fast Input Decision Ratio = double: 200
      Fast Input FIFO Bytes = int: 268435456
      FIFO Hash Mask = int: 16383
      Fast Merge Buffer Bytes = int: 536870912
      Slow Merge Buffer Bytes = int: 268435456
      Fast Merge Fan In = int: 64
      Key Cache Size Logarithm = int: 21
      Max Seeks = int: 512
      Output Old Buffer Bytes = int: 536870912
      Overflow FIFO Bytes = int: 67108864
      Paused = bool: false
      ```
   >[!NOTE]
   >
   >Fast Merge의 향상된 기능을 활용하려면 DPU당 최소 8GB의 RAM이 있는지 확인하십시오.

* **DWB 통합 업데이트를 사용한 Adobe Target**. 새로운 내보내기 파일, [!DNL ExportIntegration.exe]는 기존 를 대체합니다 [!DNL TnTSend.exe] Insight Server의 파일(`E:\Server\Scripts\TnTSend.exe`). 이 새 내보내기 파일은 두 기능을 모두 지원합니다 [Adobe Target](https://www.adobe.com/marketing/target.html) 새로운 기본 MMP(마케팅 프로필) 및 [Adobe Audience Manager](https://www.adobe.com/analytics/audience-manager.html).

   Adobe Target 내보내기에 대해 다음 명령을 업데이트해야 합니다.

   `Command = string: TnTSend.exe`

   에서

   ```
   <filepath>
   Command = string: ExportIntegration.exe
   </filepath>
   ```

   >[!NOTE]
   >
   >이 작업은 버전 6.3 이전에 만들어진 내보내기에만 영향을 줍니다.

   이전 내보내기 프로세스를 사용하려면 다음을 시도해 볼 수도 있습니다.

   * 워크스테이션에서 새 테스트 및 Target 내보내기를 만듭니다.
   * 에 있는 이전 테스트 및 Target 내보내기를 수정합니다. [!DNL Server/Profiles/`<your profile>`/내보내기.]

* **Adobe SC 프로필을 업데이트합니다.** 변경 사항 [!DNL Exclude Hit.cfg] 파일을 사용하려면 연결된 [!DNL Decoding Instructions.cfg] 파일.

   >[!NOTE]
   >
   >Adobe SC 프로필에 사용자 지정된 항목이 포함되어 있는 경우 [!DNL Decoding Instructions.cfg] 파일, [!DNL DelimitedDecoder] 매개 변수를 사용자 지정한 파일에 추가합니다.

   ```
   0 = DelimitedDecoder:
      Delimiter = string: \t
      Fields = vector: x items
      …
         5 = string:
   Changed to:
   
   5 = string: x-hit_source
   ```

   추가 [!DNL DelimitedDecoder] 필드를 사용하면 기능 업데이트를 활용하고 이러한 업데이트로 인해 발생할 수 있는 로그 처리 문제를 방지할 수 있습니다.
