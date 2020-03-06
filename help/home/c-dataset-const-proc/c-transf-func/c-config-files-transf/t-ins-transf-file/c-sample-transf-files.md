---
description: 여러 시나리오를 기준으로 Transform.cfg 파일에서 매개 변수를 지정하는 방법에 대한 정보입니다.
solution: Analytics
title: 샘플 데이터 워크벤치 Transform.cfg 파일
topic: Data workbench
uuid: cb473a5a-54e2-4bf7-84fb-c9c27910ef64
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 샘플 데이터 워크벤치 Transform.cfg 파일{#sample-data-workbench-transform-cfg-files}

여러 시나리오를 기준으로 Transform.cfg 파일에서 매개 변수를 지정하는 방법에 대한 정보입니다.

* [간단한 Insight Transform.cfg 파일](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-b7e83cafa3a947c597bd09d316930190)
* [쉼표로 구분된 값으로 출력](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-03916934ad574efc8695abbae54a1816)
* [샘플 로그 파일](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-113b3b0c0c7547ea9536bb2f465c0875)
* [웹 사이트별 로그 파일 분할 섹션](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/c-sample-transf-files.md#section-2cac205cd3934d31abb6c6ed8780196d)

각 샘플에서 파일은 데이터 워크벤치에 [!DNL Transform.cfg] 창으로 표시됩니다.

## 단순 데이터 워크벤치 Transform.cfg 파일 {#section-b7e83cafa3a947c597bd09d316930190}

다음 [!DNL Transform.cfg] [!DNL .vsl] [!DNL Logs] 창은 디렉토리에서 파일을 읽고 x-timestring 및 x-trackingid 필드를 Logs\VT 디렉토리에 저장된 텍스트 파일로 내보내는 지침을 제공합니다. 파일 순환 기간 또는 출력 파일 이름 형식이 지정되지 않았으므로 각 파일에는 하루 동안의 데이터가 들어 있으며 기본 형식의 이름이 [!DNL %yyyy%%mm%%dd%-%x-mask%.txt]있습니다.

![](assets/cfg_VisualTransform_SimpleExample.png)

## 쉼표로 구분된 값으로 출력 {#section-03916934ad574efc8695abbae54a1816}

다음 [!DNL Transform.cfg] 창에서는 로그 디렉토리에서 파일을 읽고 필드 0-13을 Logs\VT\CSV directory폴더에 저장된 쉼표로 구분된( [!DNL .vsl] [!DNL .csv]) 파일로 내보내는 지침을 제공합니다. 파일 순환 기간이 지정되지 않았으므로 각 파일에는 하루 동안의 데이터가 포함됩니다. 출력 파일은 [!DNL .csv] 형식으로 명명된 파일입니다 [!DNL %yyyy%%mm%%dd%-%x-mask%.csv].

![](assets/cfg_VisualTransform_CSVExample.png)

## 샘플 로그 파일 {#section-113b3b0c0c7547ea9536bb2f465c0875}

변환 기능을 구성하여 전체 로그 파일의 최신 압축 버전을 만들고 유지 관리할 수 있습니다. 이렇게 하면 전체 데이터 세트를 재처리하는 데 소요되는 시간(초 또는 분)이 아니라 재처리 시간을 통해 데이터 세트 구성을 신속하게 테스트할 수 있습니다. 다음 예에서는 변환 기능을 구성하는 방법의 예를 제공합니다.

다음 [!DNL Transform.cfg] [!DNL .vsl] 창은 Logs 디렉토리에서 파일을 읽고 x-timestring 및 x-trackingid 필드를 Logs\VT 디렉토리에 저장된 텍스트 파일로 내보내는 지침을 제공합니다. 지정된 해시 임계값은 데이터 세트에서 특정 추적 ID를 필터링하여 100의 배율로 샘플링되는 데이터 집합을 만듭니다. 파일 순환 기간이 지정되지 않았으므로 각 파일에는 하루 동안의 데이터가 포함됩니다. 출력 파일의 이름은 기본 [!DNL %yyyy%%mm%%dd%-%x-mask%.txt]형식입니다.

![](assets/cfg_VisualTransform_SampledExample.png)

## 웹 사이트별 로그 파일 분할 섹션 {#section-2cac205cd3934d31abb6c6ed8780196d}

다음 [!DNL Transform.cfg] 창은 Logs 디렉토리에서 [!DNL .vsl]파일을 읽고 x-timestring 및 x-trackingid 필드를 Logs\VT 디렉토리에 저장된 텍스트 파일로 내보내는 지침을 제공합니다. 정규 표현식 변환( [!DNL RETransform])은 cs-uri-stem 필드를 입력으로 가져와 사이트의 섹션을 정의하는 새 필드(x-site)를 만듭니다. x-site 필드는 출력 텍스트 파일의 이름에 포함되어 있으며, 각 파일에는 하루 동안의 데이터가 포함되어 있습니다.

![](assets/cfg_VisualTransform_SplittingExample.png)

