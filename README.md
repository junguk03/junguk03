## 정욱 · Web Security

수원대학교 정보보호학과 학생입니다. **웹 취약점 분석과 모의해킹**을 공부하고 있습니다.
직접 풀고 재현한 것만, 실패한 시도까지 기록합니다.

- Portfolio — [junguk03.github.io](https://junguk03.github.io/)
- Blog — [blog.naver.com/junkuk9503](https://blog.naver.com/junkuk9503)

## 📚 공부 중

**PortSwigger Web Security Academy** → 같은 유형 워게임 → n-day 재현 순서로 진행합니다.
진행 기록: [security_report](https://github.com/junguk03/security_report)

| 주제 | 진행 (2026-11-13) |
|---|---|
| SQL injection (Blind 포함) | 3 / 18 |
| Authentication | 시작 전 |
| OS command injection | 시작 전 |
| Access control | 시작 전 |

## 🔐 프로젝트

### GlassHouse CTF — 보안 동아리 writeup · 4인 팀 · 팀장 (2026.10 ~)

Flask로 원서 접수 서비스를 직접 만들고, 두 조로 나눠 취약점을 심은 문제를 출제한 뒤 서로 바꿔 푸는 화이트박스 CTF.

- 공통 레이아웃·컴포넌트·메인 화면, 팀 개발 가이드·CTF 규칙·출제 절차 문서, 깃 관리 담당
- 직접 출제: 02-idor, 03-bac, 04-XSS · 팀 전체 문제 9개 (Easy 4, Medium 5)
- 출제·풀이 과정을 블로그에 기록 ([소개 글](https://blog.naver.com/junkuk9503/224449794694))
- 수원대학교 IT 전공역량 강화 그룹활동 지원 프로그램 선발 (2026.10 ~ 12)
- [Write_Up_GlassHouse](https://github.com/junguk03/Write_Up_GlassHouse)

### Claude MCP Agent — 개인 · 진행 중 (2026.11 ~)

직접 만든 MCP 서버(lab-tools)를 Claude Code 에이전트에 연결해 로컬 OWASP Juice Shop을 정찰하게 하고, 결과를 사람이 직접 검증하는 학습용 실험.

- 서버 코드에서 대상 제한: 127.0.0.1·localhost만 허용, 포트 형식 검사, 리다이렉트 미추적, 본문 4000바이트 제한
- 모든 도구 호출을 허용·거부·오류로 나눠 감사 로그에 기록
- 첫 정찰(2026-11-13): Juice Shop 확인, `/ftp` 디렉터리 목록 무인증 노출 관측 · 본문 제한으로 API 경로 찾기는 실패 → 보완 계획 정리
- [Claude_MCP_Agent](https://github.com/junguk03/Claude_MCP_Agent) · [정찰 보고서](https://github.com/junguk03/Claude_MCP_Agent/blob/main/reports/261113_recon.md)

### 안심 계약 가디언 (GuardUp) — 한이음 드림업 2026 · 5인 팀 · 팀장 (2026.04 ~ 10)

자립준비청년을 위한 AI 전세 계약서 분석 앱. OCR → 개인정보 마스킹 → 공공 API → GPT-4o + RAG로 위험 조항과 위험도를 알려줍니다. Flutter 앱과 FastAPI 서버를 연동해 AWS EC2에 배포했습니다.

- Privacy-First 설계: KLUE-NER + 정규식으로 개인정보 마스킹, 외부 LLM에는 마스킹된 텍스트만 전달, 분석 후 매핑 테이블 즉시 파기
- 개발보고서·제작설계서·API 명세서 작성
- Flutter (GetX) · FastAPI · LangChain · ChromaDB · Redis · CLOVA OCR
- [Backend](https://github.com/Guard-Up/Guard_Up_Backend) · [App](https://github.com/Guard-Up/Guard_Up_App)

### 워게임 익스플로잇 코드

Dreamhack 워게임과 PortSwigger 랩을 풀며 직접 작성한 Python 익스플로잇 — [test_exploit_code](https://github.com/junguk03/test_exploit_code)

| 분류 | 내용 |
|---|---|
| SQL / NoSQL Injection | Blind SQLi 자동화, MongoDB `$regex` 추출, CouchDB `_all_docs` 조회, 객체 주입 인증 우회 |
| SSRF | 10진수 IP 표기로 필터 우회, 내부 포트 탐색 |
| Command Injection | 쿠키 값 `$(...)` 삽입, 결과 외부 전송 |
| Path Traversal → RCE | `tomcat-users.xml` 유출 → Manager로 WAR 웹셸 배포 |
| Authentication | IP 차단 우회, 에러 메시지·응답 시간 차이로 사용자명 열거 |
| Crypto | AES-CBC Padding Oracle Attack |

풀이 글: [Secret Data](https://blog.naver.com/junkuk9503/224333268246) · [Tomcat Manager](https://blog.naver.com/junkuk9503/224338403978) · [NoSQL-CouchDB](https://blog.naver.com/junkuk9503/224341863557) · [Padding Oracle](https://blog.naver.com/junkuk9503/224370201618) · [CProxy: Inject](https://blog.naver.com/junkuk9503/224471416620) 외 5편

## 🔎 재현 · 제보 · 기여

- **n-day 재현** (2026.09) — Apache 경로 조작 CVE-2021-41773 재현 ([글](https://blog.naver.com/junkuk9503/224414562448))
- **오픈소스 기여** (2026.09) — [flaskbb-plugin-conversations PR #1](https://github.com/flaskbb/flaskbb-plugin-conversations/pull/1) 머지 (디버그 코드 정리)
- **취약점 제보** (2026.10 ~ 11) — HackerOne Neon 프로그램에 보고서 1건 제출, Informative 종료 (세부 내용 비공개)

## 🏁 활동

- **WHITEHAT 2026 예선** (2026.11) — 대학생부, 4인 팀 GlassHouse로 참가. 웹·포렌식 문제 직접 풀이, 팀 900점 · 대학생부 64등 ([풀이 글](https://blog.naver.com/junkuk9503/224470305727))
- **수원대 IT 그룹활동 지원 프로그램** (2026.10 ~ 12) — GlassHouse 팀 팀장으로 선발

## 📜 자격증

- 정보처리기능사 (한국산업인력공단, 2024.04)

## 🛠 Skills

### Security

![Python](https://img.shields.io/badge/Python_(Exploit)-3776AB?logo=python&logoColor=white&style=flat-square)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square)

### Development

![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white&style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white&style=flat-square)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white&style=flat-square)
![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white&style=flat-square)

### Infra

![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white&style=flat-square)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black&style=flat-square)

## 📊 GitHub Stats

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=junguk03&layout=compact&theme=tokyonight)

## 📫 Contact

[![Portfolio](https://img.shields.io/badge/Portfolio-0E7C66?style=flat-square)](https://junguk03.github.io/)
[![Naver Blog](https://img.shields.io/badge/Naver_Blog-03C75A?logo=naver&logoColor=white&style=flat-square)](https://blog.naver.com/junkuk9503)
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white&style=flat-square)](https://github.com/junguk03)
