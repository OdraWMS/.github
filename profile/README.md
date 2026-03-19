<div align="center">
  <img src="https://raw.githubusercontent.com/OdraWMS/.github/main/docs/images/wms_ic.png" alt="WMS Icon" width="120"/>

  # OdraWMS

  PDA 기반 물류 창고 관리 시스템 (Warehouse Management System)
</div>

## 프로젝트

| 리포지토리 | 설명 | 기술 스택 |
|------------|------|-----------|
| [PDA_app](https://github.com/OdraWMS/PDA_app) | Android PDA 앱 | Kotlin, Jetpack Compose, Hilt, MVVM + Clean Architecture |
| [Server](https://github.com/OdraWMS/Server) | REST API 백엔드 서버 | Spring Boot 3.5.5, Kotlin, Spring Data JPA, MS-SQL Server |

## 시스템 아키텍처

```
┌──────────────┐     HTTP/REST     ┌──────────────┐    JDBC      ┌──────────┐
│  PDA Android │ ◄──────────────►  │  Spring Boot │ ◄──────────► │  MS-SQL  │
│     App      │       JSON        │   Server     │    JPA       │  Server  │
└──────────────┘                   └──────────────┘              └──────────┘
```

## 주요 기능

| 도메인 | 기능 |
|--------|------|
| **원자재 (ROH1)** | 입고 검수, 칭량실 이동, 창고 랙 이동, 환입 |
| **부자재 (ROH2)** | 입고 검수, 랙 이동, 생산 출고, 환입 |
| **완제품 (FERT)** | 입고 검수, 랙 이동 |
| **반제품 (HALB)** | 랙 이동, 생산 출고, 환입 |
| **재고 조회** | 원자재/부자재 검색, 로케이션별 재고 조회 |

### 부가 기능
- 사용자 인증 (로그인/로그아웃)
- 앱 버전 관리 및 자동 업데이트 (APK 다운로드)
- 다중 PDA 기기 지원 (Point Mobile, Urovo DT40, MUNBYN)
- 바코드/QR 스캔 연동

## 세부 문서

각 리포지토리의 README에서 상세 문서를 확인할 수 있습니다:
- [PDA_app README](https://github.com/OdraWMS/PDA_app#readme)
- [Server README](https://github.com/OdraWMS/Server#readme)
