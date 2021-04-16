---
description: 데이터 워크벤치 Geography와 함께 제공되는 Geography 프로필은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.
title: Geography 프로필 설치
uuid: afc0699d-e58b-481b-a3f2-ab6d6998bdd8
exl-id: 9ab07fd4-d6e7-495e-ba34-04e53c9b0aa3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 2%

---

# Geography 프로필 설치{#installing-the-geography-profile}

데이터 워크벤치 Geography와 함께 제공되는 Geography 프로필은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.

Adobe에서 제공하는 다른 모든 내부 프로필과 마찬가지로 [!DNL Geography] 프로파일은 변경할 수 없습니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

[!DNL Geography] 프로필에는 지리적 차원을 정의하는 여러 변형 데이터 세트([!DNL Dataset\Transformation\Geography] 폴더에 있음)가 포함되어 있습니다. 변형 데이터 세트 목록은 [!DNL Geography] 프로필과 함께 제공되는 파일을 포함합니다.

* [!DNL City.cfg]
* [!DNL Coordinates.cfg]
* [!DNL Country.cfg]
* [!DNL DMA.cfg]
* [!DNL Domain.cfg]

각 파일은 정의된 확장 차원에 대해 이름이 지정됩니다. 추가 파일인 [!DNL IPLookup.cfg]은 다른 변형 데이터 세트에 있는 차원을 정의하는 데 사용되는 여러 가지 지리적 데이터 필드를 정의합니다.

변형 데이터 세트에 파일이 포함된 방법에 대한 자세한 내용은 *데이터 세트 구성 안내서*&#x200B;를 참조하십시오.

**데이터 워크벤치 서버에  [!DNL Geography] 프로필을 설치하려면**

>[!NOTE]
>
>다음 설치 지침은 데이터 워크벤치를 설치하고 데이터 워크벤치 [!DNL Geography]을(를) 설치하는 데이터 워크벤치 서버와 데이터 워크벤치 서버 사이에 연결을 설정했다고 가정합니다. 아직 설치하지 않은 경우 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.

1. Adobe이 제공한 [!DNL .zip] 파일에서 Profiles 폴더를 엽니다.
1. 데이터 워크벤치 서버 설치 디렉토리의 Profiles 폴더에 [!DNL Geography] 폴더를 복사합니다. 다음 예와 같이 데이터 워크벤치 서버에 [!DNL ...\Profiles\Geography] 폴더로 종료합니다. 프로필 폴더 내의 다른 폴더 이름은 표시된 폴더 이름과 다를 수 있습니다.

   ![단계 정보](assets/Geo_installProfiles_dir.png)

1. 데이터 워크벤치 [!DNL Geography]을(를) 사용할 각 프로필에 대해 [!DNL profile.cfg] 파일을 업데이트하려면 다음 단계를 따르십시오.

   1.  [!DNL Profile Manager].
   1. [!DNL profile.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. [!DNL profile.cfg] 창이 나타납니다.

   1. [!DNL profile.cfg] 창에서 **[!UICONTROL Directories]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

      디렉토리 목록 끝에 새 디렉토리를 추가하려면 목록에서 마지막 디렉토리의 번호나 이름을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;을 클릭합니다.

   1. 새 디렉토리의 이름을 입력합니다.[!DNL Geography].
   1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL profile.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;을 클릭합니다.

      >[!NOTE]
      >
      >이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓸 때 수정된 구성 파일을 Adobe에서 제공하는 내부 프로필([!DNL Geography] 프로필 포함)에 저장하지 마십시오.
