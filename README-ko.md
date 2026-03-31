# Juicify

경험을 재사용 가능한 인사이트로 전환하세요.

Juicify는 지식을 추출하고 결정화하는 두 가지 스킬을 담은 Claude Code 플러그인입니다:

- **skill-juice** — 6렌즈 분석 프레임워크로 다른 스킬의 설계 지혜를 추출
- **work-juice** — 완료된 작업을 구조화된 케이스 스터디 리포트로 정리

## 설치

```bash
# 마켓플레이스 추가
/plugin marketplace add hminnnnnn/juicify

# 플러그인 설치
/plugin install juicify
```

## 스킬

### skill-juice

스킬이 *무엇을* 하는지가 아니라 *왜* 그렇게 설계되었는지를 분석합니다. 6개 렌즈로 인사이트를 추출합니다:

| 렌즈 | 뽑아내는 것 |
|------|------------|
| 설계 철학 | 세계관, 핵심 원칙, 해결하려는 근본 문제 |
| 시스템적 사고 | 구조적 패턴, 피드백 루프, 분리 원칙 |
| 엔지니어링 테크닉 | 원문 인용 기반의 재사용 가능한 기법 |
| 프롬프트 설계 | LLM 지시 패턴, Theory of Mind 활용 |
| 사용자 경험 | 입력 유연성, 피드백 루프, 에러 처리 |
| 내 작업에 적용 | 현재 프로젝트에 즉시 적용 가능한 구체적 인사이트 |

**사용법:**

```bash
/juicify:skill-juice brainstorming          # deep 모드 (기본값)
/juicify:skill-juice brainstorming quick    # quick 모드 (3개 렌즈)
/juicify:skill-juice ~/.claude/skills/my-skill deep
/juicify:skill-juice https://github.com/someone/skill-repo
```

**출력:** `docs/juice-notes/YYYY-MM-DD-{스킬이름}.md`에 Juice Note 저장 + 세션 요약.

### work-juice

완료된 작업 사이클(이슈 발견 → 원인 분석 → 개선 → 검증)을 구조화된 케이스 스터디 리포트로 정리합니다.

**사용법:**

```bash
/juicify:work-juice latest    # 가장 최근 케이스 리포팅
/juicify:work-juice select    # 세션의 여러 케이스 중 선택
/juicify:work-juice           # 대화형 모드 선택
```

**출력:** `docs/reports/YYYY-MM-DD-{주제}.md`에 케이스 스터디 리포트 저장

**리포트 구조:** 요약 → 현상 발견 → 원인 분석 → 개선 방향 논의 → 구현 → 검증 → 레슨런

## 왜 Juicify인가?

대부분의 사람은 스킬을 설치하고, 사용하고, 넘어갑니다. 그건 남의 도구를 빌려 쓰는 것일 뿐입니다. Juicify는 **도구 뒤에 숨은 지혜를 흡수**하도록 돕습니다 — 왜 이렇게 설계되었는지, 어떤 사고 패턴이 깔려있는지.

마찬가지로, 대부분의 작업은 완료되고 잊혀집니다. Juicify는 **모든 작업 사이클을 재사용 가능한 교훈으로 전환**하도록 돕습니다 — 무엇을 발견했는지, 다음에는 뭘 다르게 할 것인지.

## 다국어 지원

두 스킬 모두 사용자의 언어로 응답합니다. 스킬 본문은 한국어로 작성되어 있지만, 출력은 대화 언어에 맞춰 자동 적응합니다.

## 라이선스

MIT
