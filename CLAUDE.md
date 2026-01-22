# Guild Widgets - Claude Code Instructions

## 프로젝트 개요
이세계길드 Notion embed용 위젯 모음
- 주요 위젯: 뽀모도로 타이머
- 배포: GitHub Pages
- 사용처: Notion embed (iframe)

## 브랜드 가이드라인

### 컬러 팔레트
- Primary: #ffd700 (골드)
- Background: #1a1a2e → #0f3460 (다크 그라데이션)
- Accent Red: #e94560 (집중 모드)
- Accent Green: #4ade80 (휴식 모드)
- Accent Blue: #60a5fa (긴 휴식)

### 톤앤매너
- 테마: 던전 공략, RPG 느낌
- 언어: 한국어
- 무겁지 않게, 살짝 위트 있게

### 폰트 (테스트 중)
- 현재: Noto Sans KR
- 테스트 예정:
  - Pretendard
  - SUIT
  - Gmarket Sans
  - 던파 비트비트체 (게임 느낌)
  - 

## 작업 규칙

### 코드 스타일
- 단일 HTML 파일 유지 (Notion embed 편의)
- 외부 의존성 최소화
- 인라인 CSS/JS 사용

### 폰트 적용 방식
```html
<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=폰트명&display=swap" rel="stylesheet">

<!-- 로컬 폰트 -->
@font-face {
  font-family: '폰트명';
  src: url('./assets/fonts/폰트파일.woff2') format('woff2');
}
```

### Notion Embed 주의사항
- 반응형 필수 (iframe 크기 가변)
- 최소 높이: 400px 권장
- 배경 투명 또는 다크 계열

## 자주 쓰는 명령어

### Plan Mode (큰 변경 전)
```
claude --plan "폰트를 Pretendard로 변경하고 싶어"
```

### 빠른 수정
```
claude "시작 버튼 텍스트를 '던전 입장'으로 바꿔줘"
```

### 폰트 테스트
```
claude "Gmarket Sans 폰트 적용해서 미리보기 보여줘"
```

## Git 커밋 컨벤션
- feat: 새 기능
- style: 디자인/폰트 변경
- fix: 버그 수정
- docs: 문서 수정

예시:
```
git commit -m "style: Pretendard 폰트 적용"
git commit -m "feat: 타이머 완료 시 confetti 효과 추가"
```

## 배포 체크리스트
- [ ] 로컬에서 테스트 완료
- [ ] 모바일 사이즈 확인
- [ ] GitHub push
- [ ] GitHub Pages 배포 확인
- [ ] Notion embed 테스트