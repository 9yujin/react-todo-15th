# 2주차 미션: React-Todo

안녕하세요 한규진입니다!!😁

최대한 고민을 많이 해보며 진행하려고 했는데 많이 아쉽네요.
별도의 상태관리 라이브러리 없이 값들을 컴포넌트 사이로 넘기는 과정에서 중간에 한번 꼬였던 경험도 있었고, 스스로에게 많이 실망하게 만들었던 과제였습니다.. 자존감 뚝뚝

1주차 과제에 만들었던 기능에 더해서 더 많은 기능을 계획하고 있었는데 시간이 없어서 이대로 제출하는 점도 정말 아쉽습니다. <br>
3주차부터는 미리미리 하기로 스스로 약속하면서, 2주차 과제 제출합니다.

<br>

### 배포 링크


https://9yujin.github.io/react-todo-15th/

vercel로 배포하는데 자꾸 오류가 생겨서... 처음엔 `'./styles/normalize.css'` 가 오류라고 떠서 embed link 형식으로 바꿨는데도, 이번엔 다른게 뜨네요ㅠㅠ
그래서 vercel이 아닌 github page로 배포를 했습니다.

![스크린샷 2022-03-25 오전 3 46 21](https://user-images.githubusercontent.com/55226431/159988581-2e8d8e26-52e2-4038-ab99-3f24c6e4ef47.png)

<br>

### Key Questions

**1. Virtual-DOM은 무엇이고, 이를 사용함으로서 얻는 이점은 무엇인가요?**
- virtual DOM을 사용하면 실제 DOM에 접근하여 조작하는 대신, 이를 추상화한 자바스크립트 객체를 구성하여 사용합니다.
리액트에서는 아래의 세가지 절차를 밟아 웹 브라우저에 실제 DOM을 업데이트합니다. <br>
1. 데이터를 업데이트하면 전체 UI를 Virtual DOM에 리렌더링.
2. 이전 Virtual DOM에 있던 내용과 현재 내용을 비교.
3. 바뀐 부분만 실제 DOM에 적용.

**2. 미션을 진행하면서 느낀, React를 사용함으로서 얻을수 있는 장점은 무엇이었나요?**
- 1주차 과제에서는 투두 배열의 데이터가 바뀔때마다 직접 화면에 새로 그려주는 작업을 해야했는데, React를 사용하면서 상태의 변화를 감지해 재렌더링을 할 수 있게 되었습니다.

**3. React에서 상태란 무엇이고 어떻게 관리할 수 있을까요?**
- 리액트에서 state는 컴포넌트 내부에서 바뀔 수 있는 값을 의미합니다.

**4. Styled-Components 사용 후기 (CSS와 비교)**
- 가장 큰 장점은 props로 전달해주는 값을 스타일링에 쉽게 이용할 수 있는 점이었습니다. 굳이 id나 클래스를 변경해가면서 다른 스타일을 직접 적용해야하는 수고를 덜 수 있었습니다.
별도의 css파일을 만들지 않아도 되어 편했지만, 그만큼 한 파일의 길이가 길어지면서 적절히 나누는 고민을 더 하게 만들었습니다.

<br>

---

<br>
# 서론

안녕하세요 🙌🏻 프론트엔드 운영진 **김현재**입니다.

다들 1주차 미션 Vallia Todo를 멋지게 잘 수행해주신 모습이 너무 멋졌습니다! 1주차 미션을 통해 여러분들께서 본격적인 React 사용에 앞서 Vailla JS로 SPA를 만들때의 불편한 점을 느끼셨을 것 이라 생각합니다.

그리하여 이번 미션은, 1주차 스터의 미션으로 주어진 Todo list 만들기를 **React**로 리팩토링하는 것 입니다!
기존에 리액트를 잘 아시던 분들께는, 조금 더 효울적인 디자인 패턴에 대해 고민할수 있는 주차가 될 것이고, 리액트를 접해보지 못하신 분들께는 기존의 어플리케이션을 리액트로 포팅하는 과정을 통해 왜 프론트엔드 시장에 리액트가 등장하게 되었고, 리액트에서 사용하는 여러가지 방식들이 왜 바닐라에 비해 효율적인지 꺠닫는 주차가 될 것이라 생각합니다.

비교적 가벼운 미션인 만큼 코드를 짜는 데 있어 여러분의 **창의성**을 충분히 발휘해보시기 바랍니다. 작동하기만 하면 되는 것보다 같은 코드를 짜는 여러가지 방식과 패턴에 대해 많이 고민해보시고, 본인이 작성할 수 있는 가장 창의적인 방법으로 코드를 작성해주셨으면 합니다. 여러분이 미션 수행을 하는 과정에서 한 생각과 고민만큼 스터디에서 더 많은 것을 얻어가실 수 있을 것입니다.

막히는 부분이 있더라도 우선 스스로 공부하고 찾아보면서 미션을 진행하는 방식을 권고드리지만, 미션과 관련하여 운영진의 도움이 필요하시다면 얼마든지 슬랙 Q&A 채널에 질문을 남겨 주세요!

# 미션

## 예시
- [리액트 투두](https://react-todo-14th-three.vercel.app/)

## 미션 목표

- VSCode, Prettier를 이용하여 개발환경을 관리합니다.
- React의 기초를 이해합니다.
- React를 통한 어플리케이션 상태 관리 방법을 이해합니다.
- React Hooks에 대한 기초를 이해합니다.
- Styled-Components를 통한 CSS-in-JS 및 CSS Preprocessor의 사용법을 익힙니다.

## 기한

- 2022년 3월 25일(금)까지

## Key Questions

- Virtual-DOM은 무엇이고, 이를 사용함으로서 얻는 이점은 무엇인가요?
- 미션을 진행하면서 느낀, React를 사용함으로서 얻을수 있는 장점은 무엇이었나요?
- React에서 상태란 무엇이고 어떻게 관리할 수 있을까요?
- Styled-Components 사용 후기 (CSS와 비교)

## 필수 요건

- 1주차 미션의 결과물을 그대로 React로 구현합니다
- Functional Components를 사용합니다
- React Hooks만을 사용해 상태를 관리합니다 
- (이번주는 Redux, MobX, Recoil, SWR등의 외부 상태관리 라이브러리를 사용하지 않아도 미션 수행에 지장이 없습니다.)

## 선택 요건

- 기존 Todo-list에 여러분들이 추가하고 싶은 기능을 자유롭게 추가해보세요.

## 로컬 실행방법

---

`npm start` : 로컬에서 react application을 자동으로 리로드하여 실행시켜줍니다.


# 링크 및 참고자료

---

- [create react app (CRA)](https://create-react-app.dev/docs/getting-started/)
- [리액트 docs 주요 개념 1-12](https://ko.reactjs.org/docs/hello-world.html)
- [리액트 docs Hook 1-3](https://ko.reactjs.org/docs/hooks-intro.html)
- [리액트 useEffect 완벽 가이드](https://overreacted.io/ko/a-complete-guide-to-useeffect/)
- [컴포넌트 네이밍을 위한 자바스크립트 네이밍 컨벤션](https://velog.io/@cada/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8A%A4%ED%83%80%EC%9D%BC-%EA%B0%80%EC%9D%B4%EB%93%9C-%EB%84%A4%EC%9D%B4%EB%B0%8D-%EC%BB%A8%EB%B2%A4%EC%85%98-%ED%8E%B8)
- [useState, useEffect hooks](https://velog.io/@velopert/react-hooks#1-usestate)
- [styled-component](https://styled-components.com/docs/basics#getting-started)
