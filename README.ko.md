# STS2 카드 어드바이저 대시보드

실시간 카드 추천 및 덱 시너지 분석 대시보드 for **Slay the Spire 2**

> 언어: [English](README.md) · **한국어** · [中文](README.zh.md)

🎮 **모드 다운로드**: [Nexus Mods](https://www.nexusmods.com/slaythespire2/mods/627)
📊 **대시보드**: [ing-gom.github.io/sts2-card-advisor](https://ing-gom.github.io/sts2-card-advisor/)

---

## 모드 소개

게임 내 보상 화면에서 각 카드의 **티어, 시너지 점수, 추천 이유**를 오버레이로 표시하는 Slay the Spire 2 모드입니다.

### 주요 기능

- **실시간 카드 추천** — 보상 화면마다 현재 덱 기반 시너지 점수 계산
- **티어 표시** — S / A / B / C / D 등급 및 점수
- **추천 이유 태그** — 덱에서 필요한 역할(딜러/방어/스케일링 등) 기반 분석
- **넘기기 판단** — 세 카드 모두 낮은 경우 자동 스킵 추천
- **덱 스냅샷** — 보상 화면마다 덱 상태를 JSON으로 저장

### 지원 캐릭터

사일런트 / 아이언클래드 / 디펙트 / 네크로바인더 / 리젠트

---

## 대시보드 소개

이 레포는 모드와 함께 사용하는 **웹 대시보드**를 배포합니다.

### 기능

| 기능 | 설명 |
|---|---|
| 카드 카탈로그 | 전체 카드 축 태그, 티어, 시너지 역할 조회 |
| 빌드 시너지 | 카드를 픽하면 추천 카드 실시간 계산 |
| 런 스냅샷 | 게임 중 저장된 덱 상태 기록 조회 |
| 덱 시너지 분석 | 스냅샷 덱 기준 추천 카드 분석 |

### 언어

대시보드는 시스템 언어를 자동 감지하며 **한국어 / 영어 / 중국어**를 지원합니다. 헤더 우측의 **KO / EN / 中** 버튼으로 수동 전환할 수 있고, 선택한 언어는 다음 방문에도 유지됩니다 (localStorage).

### 사용 방법

**게임 실행 중 (실시간 동기화)**
1. 모드가 설치된 상태로 게임 실행
2. 브라우저에서 `http://localhost:8765` 접속
3. 보상 화면을 열 때마다 자동으로 스냅샷 동기화

**게임 없이 (카탈로그 / 과거 런 조회)**
1. [대시보드](https://ing-gom.github.io/sts2-card-advisor/) 열기
2. 사이드바 "덱 스냅샷 → 파일 선택"으로 저장된 스냅샷 불러오기
   - 저장 경로: `%APPDATA%\Sts2CardAdvisor\run_snapshots\` (Windows)
   - 저장 경로: `~/Library/Application Support/Sts2CardAdvisor/run_snapshots/` (macOS)

---

## 배포 구조

```
ing-gom/sts2-card-advisor        ← 이 레포 (공개, 대시보드 HTML만 포함)
ing-gom/sts2-card-advisor-dev    ← 개발 레포 (비공개, 전체 소스)
```

---

## License

MIT
