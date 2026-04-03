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

## Use In Codex

This repository also includes a Codex-ready skill folder:

- `codex-skills/case-brief`

Manual install:

1. Copy `codex-skills/case-brief` into `$CODEX_HOME/skills/case-brief`
2. Restart Codex

If you do not want to install a skill, use the portable prompt in:

- `prompts/case-brief-portable-prompt.md`

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
- **판단 기준 + 원천 소스 분리** — 법원이 쓴 테스트와 근거 소스를 구분해 제시

### 전문가형 근거 표기

쟁점별 결과에는 아래 필드를 함께 넣습니다.

1. **Rule** — 적용 법리
2. **Rule의 원천 소스** — 법령, 선례, 판시 문구
3. **법원의 판단 기준** — 법원이 사용한 판단 틀
4. **현재법상 활용 가능성** — 법령 개정 또는 후속 판례 반영
5. **확인일/불확실성** — 최신성 점검 시점과 추가 검토 필요 사항

### 설치

```bash
claude plugin add hslee-byte/claude-case-brief-plugin
```

### Codex에서 사용

이 저장소에는 Codex용 스킬 폴더도 포함되어 있습니다.

- `codex-skills/case-brief`

수동 설치 방법:

1. `codex-skills/case-brief` 폴더를 `$CODEX_HOME/skills/case-brief`로 복사
2. Codex 재시작

설치 없이 바로 쓰고 싶다면 아래 중립 프롬프트를 사용하면 됩니다.

- `prompts/case-brief-portable-prompt.md`

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
- 법령과 선례는 식별 가능한 단위까지 표기하고, 최신성 확인 여부를 함께 표시
- 판례 원문, 당사자 정보는 절대 기억/저장하지 않음

## License

MIT
