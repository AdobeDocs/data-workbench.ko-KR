---
description: Data WorkbenchGeography와 함께 제공된 Geography 프로필은 Adobe 응용 프로그램에 추가 기능을 제공하는 내부 프로필입니다.
title: Geography 프로필 설치
uuid: afc0699d-e58b-481b-a3f2-ab6d6998bdd8
exl-id: 9ab07fd4-d6e7-495e-ba34-04e53c9b0aa3
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 2%

---

# Geography 프로필 설치{#installing-the-geography-profile}

{{eol}}

Data WorkbenchGeography와 함께 제공된 Geography 프로필은 Adobe 응용 프로그램에 추가 기능을 제공하는 내부 프로필입니다.

Adobe이 제공하는 기타 모든 내부 프로필과 마찬가지로 [!DNL Geography] 프로필을 변경하면 안 됩니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

다음 [!DNL Geography] 프로필에는 여러 변형 데이터 세트 포함 파일( [!DNL Dataset\Transformation\Geography] 폴더)를 클릭합니다. 다음은 변환 데이터 집합 목록에 [!DNL Geography] 프로필:

* [!DNL City.cfg]
* [!DNL Coordinates.cfg]
* [!DNL Country.cfg]
* [!DNL DMA.cfg]
* [!DNL Domain.cfg]

각 파일의 이름은 파일이 정의하는 확장 차원에 대해 지정됩니다. 추가 파일, [!DNL IPLookup.cfg]에서는 다른 변형 데이터 집합에 있는 차원을 정의하는 데 사용되는 여러 가지 지리적 데이터 필드를 정의합니다. 이 필드는 파일을 포함합니다.

변형 데이터 집합에 파일이 포함된 것에 대한 자세한 내용은 *데이터 집합 구성 안내서*.

**를 설치하려면 [!DNL Geography] data workbench 서버의 프로필**

>[!NOTE]
>
>다음 설치 지침은 Data Workbench를 설치하고 Data Workbench를 설치하는 Data Workbench 서버와 Data Workbench 서버 간의 연결을 설정했다고 가정합니다 [!DNL Geography]. 아직 수행하지 않았다면 다음을 참조하십시오. *Data Workbench 사용 안내서*.

1. 에서 Profiles 폴더를 엽니다. [!DNL .zip] Adobe이 제공한 파일입니다.
1. 를 복사합니다. [!DNL Geography] 폴더를 data workbench 서버 설치 디렉토리의 Profiles 폴더로 드래그합니다. 이제 다음을 통해 [!DNL ...\Profiles\Geography] 다음 예와 같이 data workbench 서버의 폴더를 지정합니다. 프로파일 폴더 내의 다른 폴더의 이름은 표시된 폴더 이름과 다를 수 있습니다.

   ![단계 정보](assets/Geo_installProfiles_dir.png)

1. 다음 단계를 사용하여 를 업데이트합니다 [!DNL profile.cfg] data workbench를 사용할 각 프로필에 대한 파일입니다 [!DNL Geography].

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 다음 [!DNL profile.cfg] 창이 나타납니다.

   1. 에서 [!DNL profile.cfg] 창, 마우스 오른쪽 단추 클릭 **[!UICONTROL Directories]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      디렉터리 목록에 새 디렉터리를 추가하려면 목록에서 마지막 디렉터리의 번호나 이름을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. 새 디렉토리의 이름을 입력합니다. [!DNL Geography].
   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >수정된 구성 파일을 Adobe이 제공한 내부 프로필(다음을 포함)에 저장하지 마십시오 [!DNL Geography] 프로필)로 업데이트되는 경우 이러한 프로필에 업데이트를 설치하면 변경 사항을 덮어씁니다.
