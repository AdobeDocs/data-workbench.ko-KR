---
description: ExpFile 매개 변수는 실험을 정의하는 실험 구성 파일의 위치를 가리킵니다.
solution: Analytics,Analytics
title: ExpFile 매개 변수 수정
topic: Data workbench
uuid: bf146f46-f541-4969-8d90-af1a0c969344
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 3%

---


# ExpFile 매개 변수 수정{#modifying-the-expfile-parameter}

ExpFile 매개 변수는 실험을 정의하는 실험 구성 파일의 위치를 가리킵니다.

이 매개 변수를 설정하면 실험을 실행할 수 있습니다. 실험 구성 파일을 만드는 단계는 실험 구성 [및 배포를 참조하십시오](../../../home/c-undst-ctrld-exp/t-crt-ctrld-exp/c-cnfg-dply-exp.md#concept-50f1de0242904698937bb72b3ea1b429).

다음은 ExpFile 매개 변수의 예입니다.

```
ExpFile /home/experiment.txt
```

탭으로 구분된 텍스트 파일( [!DNL .txt])은 [!DNL Sensor] 폴더 내의 어느 곳에서나 찾을 수 있으며 편리한 이름을 가질 수 있습니다.

실험 구성 파일을 저장하고 이 이름과 이 디렉토리에 대해 자세히 설명하려면 실험 디렉토리의 위치와 지정한 구성 파일의 이름을 기록해야 합니다.

>[!NOTE]
>
>이 매개 변수가 설치되어 있는 웹 클러스터의 각 시스템에서 동일하게 설정되지 않으면 제어된 실험 [!DNL Sensor] 이 작동하지 않습니다.

이 항목은 구성 파일에 사전 구성할 수 있으며 [!DNL Sensor] 구성 파일에 계속 남아 있을 수 있으며 부작용이 없습니다. 지정한 실험 구성 파일 이름을 찾을 수 없거나 비어 있는 경우(즉, 존재하지만 컨텐츠가 없는 경우), 테스트를 수행하지 [!DNL Sensor] [!DNL Sensor] 않고 HTTP 서버에 오류 이벤트를 기록하고 다른 모든 면에서 정상적으로 계속 작동합니다.
