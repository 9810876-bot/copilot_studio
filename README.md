# 광탄중학교 챗봇 프렌 🤖

광탄중학교 학생들을 위한 AI 챗봇 "프렌(PREN)" 프로젝트입니다.

## 📖 개요

이 프로젝트는 **Microsoft Copilot Studio**를 활용하여 만든 웹 기반 챗봇 인터페이스입니다. 학생들이 학교 관련 궁금한 점을 언제든지 쉽게 질문할 수 있도록 설계되었습니다.

## ✨ 주요 특징

- 🎨 **파스텔톤 UI**: 산뜻하고 친근한 한글 기반 디자인
- 📱 **반응형 디자인**: 모바일, 태블릿, 데스크톱 모두 지원
- 💬 **실시간 대화**: Microsoft Bot Framework Web Chat 기반
- 🌈 **맞춤형 스타일링**: 학교 브랜드에 맞춘 색상 테마
- ♿ **접근성**: 의미있는 HTML 구조와 ARIA 속성

## 🛠️ 기술 스택

- **프론트엔드**: HTML5, CSS3, Vanilla JavaScript
- **챗봇 엔진**: Microsoft Copilot Studio
- **통신**: Direct Line API (v3)
- **폰트**: Google Fonts (Gowun Dodum, Jua)

## 📋 필수 설정

### 토큰 엔드포인트 설정

`index.html` 파일의 다음 부분을 수정하세요:

```javascript
const tokenEndpoint = "https://your-endpoint-url/powervirtualagents/...";
```

**설정 방법:**
1. Microsoft Copilot Studio에서 봇을 생성합니다
2. "채널" > "Direct Line" 섹션에서 토큰 엔드포인트를 복사합니다
3. 위의 코드에 붙여넣습니다

## 🎨 색상 커스터마이징

`index.html`의 `styleOptions` 객체에서 색상을 수정할 수 있습니다:

```javascript
const styleOptions = {
  accent: "#8FD3C4",                    // 강조색
  bubbleBackground: "#E7F6F0",          // 봇 말풍선
  bubbleFromUserBackground: "#FDEDE2",  // 사용자 말풍선
  // ... 더 많은 옵션
};
```

또는 CSS 변수로도 조정 가능합니다:

```css
:root {
  --mint: #C5EDE0;
  --sky: #C7E6F5;
  --peach: #FCE0CE;
  /* ... */
}
```

## 📖 사용 방법

1. 이 저장소를 클론합니다
2. `index.html`의 토큰 엔드포인트를 설정합니다
3. 웹 서버에서 `index.html`을 호스팅합니다
4. 브라우저에서 접속하여 사용합니다

### GitHub Pages에서 호스팅하기

1. 저장소 설정 > Pages에서 배포 소스를 "main branch"로 설정
2. `https://yourusername.github.io/copilot_studio/` 에서 접속 가능

## 🔧 주요 코드 설명

### 초기화 함수

```javascript
async function initializeChat() {
  // 1. Regional Channel Settings 조회
  // 2. Direct Line 토큰 요청
  // 3. Web Chat 렌더링
}
```

### 커스텀 스토어

```javascript
function createCustomStore() {
  // 챗봇 연결 시 자동으로 대화 시작
}
```

## 📁 파일 구조

```
copilot_studio/
├── index.html       # 메인 챗봇 인터페이스
├── README.md        # 이 파일
└── .gitignore       # Git 무시 파일 (선택)
```

## 🐛 문제 해결

### "챗봇을 불러오지 못했어요" 에러

- ✅ 토큰 엔드포인트가 올바르게 설정되어 있는지 확인
- ✅ Copilot Studio에서 봇이 "게시됨" 상태인지 확인
- ✅ 브라우저 개발자 도구(F12) 콘솔에서 에러 메시지 확인

### CORS 에러

- ✅ 올바른 환경(Power Platform)의 엔드포인트 사용
- ✅ 봇의 Direct Line 채널이 활성화되어 있는지 확인

## 📞 지원

문제가 발생하면 다음을 확인하세요:

1. [Microsoft Bot Framework 문서](https://docs.microsoft.com/en-us/azure/bot-service/)
2. [Web Chat 라이브러리](https://github.com/microsoft/BotFramework-WebChat)
3. 브라우저 콘솔 로그

## 📝 라이선스

이 프로젝트는 교육용 목적으로 제작되었습니다.

## 🙏 감사의 말

- Microsoft Bot Framework 팀
- Google Fonts
- 광탄중학교 커뮤니티

---

**"프렌"과 함께 궁금한 것들을 편하게 해결해보세요! 🌟**
