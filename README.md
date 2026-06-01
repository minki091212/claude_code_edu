# 프로그래밍 학습 강사 (Claude Code 설정)

어떤 언어·프레임워크를 배우든 Claude를 "강사"로 만들어주는 설정.

## 폴더 구조
```
learning-tutor/
├── CLAUDE.md              # 매 세션 자동 적용되는 강사 설정 (핵심)
├── CURRICULUM.md          # 로드맵 + 진도 (필요할 때만 읽힘)
└── .claude/commands/      # 필수 4기능 슬래시 명령
    ├── review.md          # /review  — 코드 리뷰
    ├── concept.md         # /concept — 개념 강의
    ├── hint.md            # /hint    — 힌트 주기
    └── debug.md           # /debug   — 같이 에러 디버깅
```

## 사용법
1. 이 폴더 안에서 `claude` 실행 → CLAUDE.md가 자동 적용됨.
2. 첫 마디로 배울 기술을 정한다. 예: "오늘부터 C++ 배울 거야. 로드맵부터 같이 짜자."
3. 필요할 때 슬래시 명령 사용: `/concept 포인터`, `/hint`, `/review`, `/debug <에러>`
   (평범한 말로 "이거 리뷰해줘"라고 해도 동작함)

## 참고
- `.claude/commands/`는 현재도 동작하는 방식이며, 최신 Claude Code에서는
  `.claude/skills/<이름>/SKILL.md`로 올려도 같은 `/이름`으로 호출된다. 지금은 이대로 충분.
- Claude가 자꾸 같은 실수를 하면 "그거 막게 CLAUDE.md 고쳐줘"라고 시키면 점점 내게 맞춰진다.

## 웹 서치
- `.claude/settings.json`에서 `WebSearch`/`WebFetch`를 미리 허용해 뒀다(읽기 전용이라 안전).
- Claude가 최신 버전·공식 문서를 확인해 가르치고, 에러도 최신 정보로 같이 디버깅한다.
- 만약 그래도 도메인마다 승인 창이 뜨면, 뜰 때 "이 도메인 항상 허용"을 한 번 골라주면 된다.
  (Claude Code 버전에 따라 권한 동작에 차이가 있을 수 있다.)
