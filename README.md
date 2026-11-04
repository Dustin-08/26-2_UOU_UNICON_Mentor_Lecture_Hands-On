# 🧩 나만의 웹 위젯 만들기 실습

> AI(Gemini, Claude 등)에게 말만 걸어서 **노션 포트폴리오에 넣을 수 있는 위젯**을 뚝딱 만들어보는 강연 실습 자료입니다.
> 코딩을 몰라도 괜찮아요. 복사 → 붙여넣기 → 말로 고치기, 이 세 단계면 충분합니다!

---

## 🎯 이 저장소로 할 수 있는 것

1. 완성된 위젯 코드를 **다운로드해서 바로 실행**해보기
2. **프롬프트를 복사**해서 AI에게 붙여넣고 나만의 위젯 만들기
3. 만든 위젯을 **노션 페이지에 임베드**하기

---

## 🗂 위젯 목록

| 위젯 | 파일 | 설명 | 미리보기 |
|------|------|------|---------|
| ⏳ D-Day 카운트다운 | [`timerWidget.html`](./timerWidget.html) | 목표일까지 남은 일/시/분/초를 실시간 표시 | [열어보기](https://Dustin-08.github.io/26-2_UOU_UNICON_Mentor_Lecture_Hands-On/timerWidget.html) |
| 🚀 기술 스택 카드 | [`interac_card.html`](./interac_card.html) | 마우스를 올리면 3D로 뒤집히는 카드 | [열어보기](https://Dustin-08.github.io/26-2_UOU_UNICON_Mentor_Lecture_Hands-On/interac_card.html) |
| 💬 오늘의 명언 | [`myeongun.html`](./myeongun.html) | 새로고침할 때마다 명언이 랜덤으로 바뀜 | [열어보기](https://Dustin-08.github.io/26-2_UOU_UNICON_Mentor_Lecture_Hands-On/myeongun.html) |
| ⚡ 스킬 게이지 | [`progressbar.html`](./progressbar.html) | 로딩 시 게이지가 스르륵 차오르는 애니메이션 | [열어보기](https://<아이디>.github.io/<저장소이름>/progressbar.html) |
| 📝 방명록 / 한줄 메모 | [`guest.html`](./guest.html) | 한줄 메모를 등록·삭제 (브라우저에 저장) | [열어보기](https://Dustin-08.github.io/26-2_UOU_UNICON_Mentor_Lecture_Hands-On/guest.html) |
| 🔗 소셜 링크 | [`profile.html`](./profile.html) | GitHub·메일·LinkedIn·Instagram 버튼 모음 | [열어보기](https://Dustin-08.github.io/26-2_UOU_UNICON_Mentor_Lecture_Hands-On/profile.html) |

---

## 🚀 사용 방법

### 방법 1. 코드 그대로 실행해보기

1. 이 저장소 우측 상단의 **Code → Download ZIP** 클릭
2. 압축을 풀고, 원하는 `.html` 파일을 **더블클릭**
3. 브라우저에서 위젯이 열리면 성공! 🎉

### 방법 2. AI로 나만의 위젯 만들기 (추천!)

1. [`PROMPTS.md`](./PROMPTS.md)를 열어요
2. 마음에 드는 프롬프트를 **통째로 복사**해요
3. [Gemini](https://gemini.google.com) 또는 [Claude](https://claude.ai)에 **붙여넣기**
4. 나온 코드를 메모장에 붙여넣고 `파일이름.html`로 저장
5. 마음에 안 드는 부분은 **말로 고쳐달라고** 요청해요

### 방법 3. 노션에 임베드하기

1. 이 저장소를 **GitHub Pages**로 공개해요 (아래 참고)
2. 노션 페이지에서 `/embed` 입력 → 위젯 주소 붙여넣기
   예: `https://<아이디>.github.io/<저장소이름>/timerWidget.html`
3. 크기를 드래그로 조절하면 끝!

---

## 🌐 GitHub Pages로 공개하기

1. 저장소 상단 **Settings** 클릭
2. 왼쪽 메뉴 **Pages** 선택
3. **Source**를 `Deploy from a branch`, Branch를 `main` / `(root)`로 설정 후 **Save**
4. 1~2분 뒤 `https://<아이디>.github.io/<저장소이름>/` 주소로 접속 가능

---

## 🛠 수정이 필요할 때 (자주 바꾸는 곳)

| 위젯 | 바꾸고 싶은 것 | 코드에서 찾을 곳 |
|------|---------------|-----------------|
| D-Day | 목표 날짜 | `new Date(2026, 11, 31, ...)` ※ 월은 0부터 시작 (11 = 12월) |
| D-Day | 제목 문구 | `<h2 id="title">` 안의 텍스트 |
| 명언 | 명언 목록 | `const quotes = [ ... ]` 배열 |
| 스킬 게이지 | 항목·퍼센트 | `data-width="90%"` 와 옆의 `90%` 숫자 |
| 기술 카드 | 기술 이름·설명 | `.card-front`, `.card-back` 안의 텍스트 |
| 소셜 링크 | 내 링크 | `href="..."` 주소 |

> 💡 코드를 직접 고치기 어렵다면 AI에게 코드를 붙여넣고 "명언을 이걸로 바꿔줘"라고 말해보세요!

---

## ⚠️ 참고사항

- **방명록(`guest.html`)의 메모는 내 브라우저에만 저장**됩니다. 다른 사람이 남긴 글이 보이는 진짜 방명록이 아니라, 연습용 한줄 메모장이에요. 여러 사람이 함께 쓰려면 별도의 데이터베이스가 필요합니다.
- 노션 임베드는 **공개된 주소(https)** 만 가능합니다. 내 컴퓨터에만 있는 파일은 임베드되지 않아요.
- 폰트는 `Pretendard`를 지정했지만 따로 불러오지 않았기 때문에, 설치되어 있지 않은 환경에서는 기본 폰트로 보일 수 있습니다.

---

## 📚 더 알아보기

- 프롬프트 작성법과 복사용 예시 → [`PROMPTS.md`](./PROMPTS.md)
- 질문이나 개선 아이디어는 **Issues** 탭에 남겨주세요 😊

---

## 📄 라이선스

수강생 여러분이 자유롭게 복사·수정·활용하셔도 좋습니다. 마음껏 가져가서 나만의 위젯으로 만들어보세요! 🎈