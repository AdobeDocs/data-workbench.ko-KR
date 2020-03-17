---
description: 데이터 워크벤치 6.3용 서버 구성 요소를 업그레이드합니다.
title: DWB Server 업그레이드 6.2 - 6.3
uuid: e12b6cc1-070e-4bc7-bc64-203d11cfeae9
translation-type: tm+mt
source-git-commit: 79d5a2f44ade88f25f7621a4738d14c43777fc9f

---


# DWB Server 업그레이드:6.2 - 6.3{#dwb-server-upgrade-to}

데이터 워크벤치 6.3용 서버 구성 요소를 업그레이드합니다.

**업그레이드 서버**

패키지에 제공된 기본 파일보다 우선하는 프로파일을 사용자 정의한 경우 [!DNL Base] 이러한 사용자 정의 파일을 업데이트해야 합니다.

* **Meta.cfg 파일을** 업데이트(FSU 서버) [!DNL E:\..\Profiles\<your custom profile>\Context\meta.cfg)]하여 업데이트된 암호 암호화를 설정하고, 쿼리 문자열 그룹을 활용할 수 있도록 이름 값 쌍 변형에 대한 항목을 [추가합니다](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-2-to-6-3-upgrade.md#concept-42f74911b5714219a359b719badac8e0).

   1. FSU에서 파일을 [!DNL meta.cfg] 엽니다.
   1. 워크스테이션 구성 섹션에서 **[!UICONTROL Proxy Password]** &quot; [!DNL string"] 에서 &quot;&quot; [!DNL EncryptedString]로 데이터 유형을 *변경합니다* .

      ```
        Proxy User Name = string: 
        Proxy Password = EncryptedString:   ( 
        from Proxy Password = String) 
        Use Address File = bool: true
      ```

   1. 새 항목을 추가하여 새로운 이름 값 쌍 변형을 활성화합니다.BuildNameValuePair *및* ExtractNameValuePairs **.

      작업 영역을 열고 관리 > **프로필 관리자를** 마우스 오른쪽 단추로 **클릭합니다**.

      Context **에서 Base**&#x200B;열의 **meta.cfg** 파일을 **클릭한 다음** Make Local **을**&#x200B;클릭합니다. 사용자 테이블 열에서 마우스 오른쪽 단추를 클릭하고 **워크스테이션에서 열기** > **를 선택합니다**.

      ![](assets/meta_cfg.png)

      * 새 창에서 **메타데이터를** 클릭하고 허용되는 하위 템플릿을 추가합니다.

         ![](assets/meta_cfg_child.png)

      * 변형을 **열고** 새 템플릿을 추가합니다.

         ![](assets/meta_cfg_template.png)

* **빠른 병합을 위한 업데이트 개선**&#x200B;사항 변환 중 데이터 워크벤치의 속도 개선을 활용하려면 다음 구성 파일에 매개 변수를 추가하거나 값을 변경합니다.

   * **Communications.cfg** ( [!DNL E:\Server\Components\Communications.cfg])

      ```
      18 = SourceListServer:  
          URI = string: /SourceListServer/ 
          Listing Interval = int: 10 ( 
      <new>)
      ```

   * **Disk Files.cfg** ( [!DNL E:\Server\Components] 및 [!DNL E:\Server\Components for Processing Servers])

      ```
      Disk Cache Size (MB) = double: 1024  
      <(from double: 256)> 
      Disk Cache Read Limit (MB) = double: 768  
      <(new)>
      ```

   * **로그 처리 모드.cfg** ( [!DNL E:\Server\Profiles\<your profile>\Dataset\Log Processing Mode.cfg])

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
   >향상된 빠른 병합 기능을 활용하려면 DPU당 최소 8GB의 RAM이 있어야 합니다.

* **DWB 통합 업데이트가**&#x200B;포함된 Adobe Target 새 내보내기 파일이 Insight [!DNL ExportIntegration.exe]Server( [!DNL TnTSend.exe]`E:\Server\Scripts\TnTSend.exe`)의 기존 파일을 대체합니다. 이 새로운 내보내기 파일은 Adobe [Target](https://www.adobe.com/marketing/target.html) 통합 및 새로운 MMP(Master Marketing Profile) 및 Adobe Audience Manager와의 조정을 모두 [지원합니다](https://www.adobe.com/analytics/audience-manager.html).

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
   >이는 버전 6.3 이전에 생성된 내보내기에만 영향을 줍니다.

   이전 내보내기 프로세스를 적용하기 위해 다음을 시도할 수도 있습니다.

   * 워크스테이션에서 새 테스트 및 대상 내보내기를 만듭니다.
   * /Export에 있는 이전 테스트 및 대상 내보내기를 [!DNL Server/Profiles/`<your profile>`수정합니다.]

* **Adobe SC 프로필을 업데이트합니다.** 파일을 변경하면 관련 [!DNL Exclude Hit.cfg] [!DNL Decoding Instructions.cfg] 파일에서 필드를 선언해야 합니다.

   >[!NOTE]
   >
   >Adobe SC 프로필에 사용자 정의된 [!DNL Decoding Instructions.cfg] 파일이 포함되어 있는 경우 사용자 지정된 파일에 [!DNL DelimitedDecoder] 매개 변수를 포함해야 합니다.

   ```
   0 = DelimitedDecoder: 
      Delimiter = string: \t 
      Fields = vector: x items 
      …  
         5 = string: 
   Changed to: 
   
   5 = string: x-hit_source
   ```

   이 [!DNL DelimitedDecoder] 필드를 추가하면 기능 업데이트를 활용하고 이러한 업데이트로 인해 발생할 수 있는 로그 처리 문제를 방지할 수 있습니다.
