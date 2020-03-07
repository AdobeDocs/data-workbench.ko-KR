---
description: 데이터 workbenchGeography와 함께 제공되는 지리 프로필은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.
solution: Analytics
title: 지역 프로필 설치
topic: Data workbench
uuid: afc0699d-e58b-481b-a3f2-ab6d6998bdd8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 지역 프로필 설치{#installing-the-geography-profile}

데이터 workbenchGeography와 함께 제공되는 지리 프로필은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.

Adobe에서 제공한 다른 모든 내부 프로필과 마찬가지로 프로필을 변경하면 [!DNL Geography] 안 됩니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

이 [!DNL Geography] 프로필에는 지리적 차원을 정의하는 파일( [!DNL Dataset\Transformation\Geography] 폴더에 있음)이 포함된 여러 변형 데이터 세트가 포함되어 있습니다. 변형 데이터 세트 목록에는 [!DNL Geography] 프로필과 함께 제공된 파일이 포함되어 있습니다.

* [!DNL City.cfg]
* [!DNL Coordinates.cfg]
* [!DNL Country.cfg]
* [!DNL DMA.cfg]
* [!DNL Domain.cfg]

각 파일의 이름은 파일이 정의하는 확장 차원에 따라 지정됩니다. 다른 변형 데이터 세트에 있는 차원을 정의하는 데 사용되는 여러 가지 지역 데이터 필드를 [!DNL IPLookup.cfg]정의하는 추가 파일은 파일을 포함합니다.

변형 데이터 세트에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오*.

**데이터 워크벤치 서버에[!DNL Geography]프로파일을 설치하려면**

>[!NOTE]
>
>다음 설치 지침은 데이터 워크벤치를 설치하고 데이터 워크벤치를 설치하는 데이터 워크벤치와 데이터 워크벤치 서버 사이에 연결을 설정했다고 가정합니다 [!DNL Geography]. 이렇게 하지 않은 경우 데이터 워크벤치 *사용 안내서를 참조하십시오*.

1. Adobe에서 제공한 [!DNL .zip] 파일에서 Profiles 폴더를 엽니다.
1. 데이터 워크벤치 서버 설치 디렉토리의 Profiles 폴더에 [!DNL Geography] 폴더를 복사합니다. 다음 예와 같이 데이터 워크벤치 서버의 [!DNL ...\Profiles\Geography] 폴더로 마무리하려고 합니다. Profiles 폴더 내의 다른 폴더 이름과 다를 수 있습니다.

   ![단계 정보](assets/Geo_installProfiles_dir.png)

1. 데이터 워크벤치를 사용할 각 프로필에 대한 [!DNL profile.cfg] 파일을 업데이트하려면 다음 단계를 [!DNL Geography]사용합니다.

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL profile.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 창이 [!DNL profile.cfg] 나타납니다.

   1. 창에서 [!DNL profile.cfg] 마우스 오른쪽 단추를 **[!UICONTROL Directories]** 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

      디렉토리 목록 끝에 새 디렉토리를 추가하려면 목록에서 마지막 디렉토리의 번호나 이름을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

   1. 새 디렉토리의 이름을 입력합니다. [!DNL Geography]Adobe
   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL profile.cfg] > [!DNL User] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL profile name]***.

      >[!NOTE]
      >
      >이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필( [!DNL Geography] 프로필 포함)에 저장하지 마십시오.

