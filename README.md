# Case Brief — 판례 IRAC 요약

> [한국어](#한국어)

A Claude Code plugin that summarizes court decisions into structured IRAC format. Input a case number, paste decision text, or provide a file — get Issue, Rule, Application, Conclusion with practice implications.

## What It Does

```
Case text or number → IRAC summary → Practice implications → Usable output
```

### Analysis Flow

| Phase | What happens |
|---|---|
| **0. Read & Context** | Auto-detect court, case type, parties. Ask review perspective |
| **1. IRAC Summary** | Structured Issue/Rule/Application/Conclusion for each legal point |
| **2. Practice Implications** | What changes, when to cite, counter-arguments |
| **3. Output** | IRAC brief / 1-page summary / Citation format / Comparison table |

### Key Features

- **Multi-issue support** — Numbers each issue in court's judgment order
- **Rule with citations** — Statute article/paragraph/subparagraph + prior precedents
- **Verbatim key holdings** — Critical passages quoted from original, not paraphrased
- **Counter-arguments** — Points where opposing counsel could distinguish the case
- **Citation-ready output** — "대법원 2024. 1. 1. 선고 2024다12345 판결 참조" format

## Install

```bash
claude plugin add hslee-byte/claude-case-brief-plugin
```

## Usage

```
/case-brief 2024다12345
/case-brief /path/to/decision.pdf
/case-brief
```

## Output Options

1. **IRAC Brief** — Full structured summary
2. **1-Page Summary** — Issues + conclusion + implications only
3. **Citation Format** — Ready to paste into legal briefs
4. **Comparison Table** — Side-by-side when multiple cases provided

---

## 한국어

판례 텍스트 또는 사건번호를 넣으면 IRAC 구조로 요약하고 실무 시사점을 도출하는 Claude Code 플러그인. 변호사, 변리사, 노무사, 세무사를 위해 만들었습니다.

### 분석 흐름

```
판례 입력 → 법원/사건유형 파악 → IRAC 요약 → 실무 시사점 → 결과물 출력
```

### 특징

- **쟁점별 IRAC** — 법원 판단 순서대로 번호 매기기
- **근거 법령 + 선례** — 조/항/호까지 명시, 관련 판례 인용
- **핵심 판시 원문 인용** — 요약하되 변형하지 않음
- **반대 논거** — 상대방이 "이 사건과 다르다"고 주장할 수 있는 포인트
- **서면 인용문** — 준비서면에 바로 붙일 수 있는 형태

### 설치

```bash
claude plugin add hslee-byte/claude-case-brief-plugin
```

### 사용법

```
/case-brief 2024다12345
/case-brief 판례파일.pdf
/case-brief
```

### 결과물

1. **IRAC 요약** — 전체 구조화 요약
2. **1페이지 브리프** — 쟁점/결론/시사점만
3. **서면 인용문** — 준비서면에 바로 붙이는 형태
4. **비교표** — 여러 판례 입력 시 쟁점별 비교

### 안전장치

- 모든 결과물 상단에 "⚠️ AI 보조 요약입니다. 원문 확인을 권고합니다." 표시
- 판례 원문의 핵심 판시는 반드시 원문 인용 (변형하지 않음)
- 판례 원문, 당사자 정보는 절대 기억/저장하지 않음

## License

MIT
