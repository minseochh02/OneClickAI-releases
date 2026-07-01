# 원클릭로그인 (OneClick AI)

**원클릭로그인**은 웹사이트 로그인을 한 번 녹화해 두고, 이후에는 클릭 한 번으로 자동 로그인하는 Windows 데스크톱 앱입니다.

> 이 저장소는 **설치 파일 배포 및 자동 업데이트** 전용입니다.  
> 소스 코드는 [egdesk-scratch](https://github.com/minseochh02/egdesk-scratch) 모노레포에서 관리됩니다.

---

## 주요 기능

- **Browser Recorder** — Chrome에서 로그인·클릭 동작을 녹화해 재사용 가능한 스크립트로 저장
- **원클릭 로그인** — 저장된 사이트 계정을 선택해 순차적으로 자동 로그인
- **자동 업데이트** — 앱 실행 시 새 버전 확인 (설정에서 켜기/끄기 가능)

---

## 다운로드

[Releases](https://github.com/minseochh02/OneClickAI-releases/releases)에서 최신 버전을 받으세요.

| 파일 | 설명 |
|------|------|
| `원클릭로그인 Setup x.x.x.exe` | Windows 설치 프로그램 (권장) |
| `latest.yml` | 앱 자동 업데이트용 메타데이터 (직접 설치 불필요) |

---

## 시스템 요구 사항

- **OS:** Windows 10 / 11 (64-bit)
- **브라우저:** Google Chrome (Browser Recorder·자동 로그인용)
- **기타:** 인터넷 연결 (업데이트 확인 및 대상 사이트 접속)

---

## 사용 방법

1. **원클릭로그인**을 설치하고 실행합니다.
2. **Browser Recorder** 탭에서 로그인 URL을 입력하고 **녹화 시작**을 누릅니다.
3. Chrome에서 로그인한 뒤 필요한 동작을 수행하고 녹화를 중지합니다.
4. **원클릭 로그인** 탭에서 저장된 계정을 선택해 **원클릭로그인 시작**을 누릅니다.

---

## 자동 업데이트

패키징된 앱은 이 저장소의 GitHub Releases를 업데이트 소스로 사용합니다.

- 앱 → **설정**에서 자동 업데이트를 켤 수 있습니다.
- 새 버전이 있으면 앱 내 알림으로 안내됩니다.

---

## 관련 앱

| 앱 | Releases 저장소 | 용도 |
|----|-----------------|------|
| **원클릭로그인** | [OneClickAI-releases](https://github.com/minseochh02/OneClickAI-releases) | 웹사이트 로그인 녹화·자동 로그인 |
| **인터넷뱅킹AI** | [InternetBankingAI-release](https://github.com/minseochh02/InternetBankingAI-release) | 은행·카드·홈택스·고용24 자동화 |
| **EGDesk** | [egdesk-scratch](https://github.com/minseochh02/egdesk-scratch/releases) | 전체 EGDesk 플랫폼 |

원클릭로그인과 인터넷뱅킹AI는 동일한 사용자 데이터 폴더(`egdesk`)를 공유할 수 있습니다.

---

## 문의 및 버그 리포트

문제가 있으면 [Issues](https://github.com/minseochh02/OneClickAI-releases/issues)에 등록해 주세요.

---

## 개발자용 — 릴리스 게시

소스 저장소에서 Windows 릴리스를 이 repo로 게시합니다:

```bash
pnpm setup:oneclick
pnpm --filter oneclick release:win
