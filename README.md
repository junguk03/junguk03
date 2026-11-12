## 정욱 · Web Security

수원대학교 정보보호학과 학생입니다. **웹 취약점 분석과 모의해킹**을 공부하고 있습니다.
직접 풀고 재현한 것만, 실패한 시도까지 기록합니다.

- Portfolio — [junguk03.github.io](https://junguk03.github.io/)
- Blog — [blog.naver.com/junkuk9503](https://blog.naver.com/junkuk9503)

## 📚 공부 중

**PortSwigger Web Security Academy** → 같은 유형 워게임 → n-day 재현 순서로 진행합니다.
진행 기록: [security_report](https://github.com/junguk03/security_report)

| 주제 | 진행 (2026-11-11) |
|---|---|
| SQL injection (Blind 포함) | 3 / 18 |
| Authentication | 시작 전 |
| OS command injection | 시작 전 |
| Access control | 시작 전 |

## 🔐 프로젝트

### GlassHouse CTF — 보안 동아리 · 4인 팀 · 팀장 (2026.10 ~)

Flask로 원서 접수 서비스를 직접 만들고, 두 조로 나눠 취약점을 심은 문제를 출제한 뒤 서로 바꿔 푸는 화이트박스 CTF.

- 공통 레이아웃·컴포넌트·메인 화면과 깃 관리 담당
- 문제 8개: IDOR, SQL Injection, 파일 다운로드, Broken Access Control, Mass Assignment, SSTI, Race Condition 등
- [Write_Up_GlassHouse](https://github.com/junguk03/Write_Up_GlassHouse)

### 안심 계약 가디언 (GuardUp) — 한이음 드림업 2026 · 5인 팀 · 팀장

자립준비청년을 위한 AI 전세 계약서 분석 앱. OCR → 개인정보 마스킹 → 공공 API → GPT-4o + RAG로 위험 조항과 위험도를 알려줍니다.

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

## 🏁 활동

- **WHITEHAT 2026** (2026.11) — 대학생부, 팀 GlassHouse(수원대학교)로 온라인 예선 참가

## 🛠 Tech

Burp Suite · Python · Flask · FastAPI · Node.js · Flutter · Docker · Redis · Linux
