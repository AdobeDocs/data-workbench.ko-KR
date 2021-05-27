---
description: 첫 번째 단계는 대시보드 서버에서 IIS 역할을 활성화하는 것입니다.
title: IIS 활성화
uuid: fbd194db-3307-41ae-8ece-05eb261d74ad
exl-id: 0d431302-1e69-49b6-8757-9823fd70a3b4
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# IIS 활성화{#enabling-iis}

첫 번째 단계는 대시보드 서버에서 IIS 역할을 활성화하는 것입니다.

1. **[!UICONTROL Administrative Tools]**&#x200B;에서 **[!UICONTROL Server Manager]**&#x200B;을 엽니다.
1. **[!UICONTROL Server Manager]** 창의 왼쪽에 있는 역할 메뉴 항목을 마우스 오른쪽 단추로 클릭합니다.
1. **[!UICONTROL Add Roles]**&#x200B;을 선택합니다.
1. **[!UICONTROL Web Server (IIS)]** 을 선택하고 **[!UICONTROL Add Roles Wizard]** 을 계속 진행합니다. 다음 역할 서비스가 활성화되어 있는지 확인합니다.

   | 일반적인 HTTP 기능 |
   |---|
   | 정적 콘텐츠 |
   | 기본 문서 |
   | 디렉터리 검색 |
   | HTTP 오류 |
   | HTTP 리디렉션 |

   | 애플리케이션 개발 |
   |---|
   | ASP.NET |
   | .NET 확장성 |
   | ISAPI 확장 |
   | ISAPI 필터 |

   | 상태 및 진단 |
   |---|
   | HTTP 로깅 |
   | 로깅 도구 |
   | 요청 모니터 |
   | 추적 |
   | 사용자 지정 로깅 |

   | 보안 |
   |---|
   | 기본 인증 |
   | Windows 인증 |
   | URL 인증 |
   | 요청 필터링 |
   | IP 및 도메인 제한 |

   | 관리 도구 |
   |---|
   | IIS 관리 콘솔 |
   | IIS 관리 스크립트 및 도구 |
   | 관리 서비스 |

1. 마법사를 따라 설치를 완료합니다.
