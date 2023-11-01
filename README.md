# CSS UI Simulation

:animation, box-shadow등 익숙하지 않은 css 프로퍼티를 쉽게 사용하기 위해 UI로 설정하고 확인할 수 있는 반응형 web

## Stack, lib

- typescript
- react-router
- react-icons
- extension
  - prettier
  - github copilot

## 단일 Page

## UI(Components)

- Header

  - Button
    - navigation-on: navigation 목록을 출력하는 버튼
    - history-on: history 목록을 출력하는 버튼

- Tab: 모바일 화면 크기에서는 컴포넌트를 확대

  - Left: navigation 목록
    - Overlay
    - List
      - Item
  - Right: history 목록
    - Overlay
    - Button
      - 숨김: 해당 탭을 숨김
      - 확대: 탭을 확대
    - List
      - Item: 접근한 프로퍼티 페이지, 복사한 프로퍼티 설정

- Main
  - Box1: css 프로퍼티 설명
  - Box2: css 프로퍼티 속성 값 제어(input)
  - Screen: 설정된 css 프로퍼티 UI
    - Button: 설정 값 복사

## 요구사항

### Logic

history

```javascript
// localStorage data
[
  {
    property: 'box-shadow',
    copyValues: [],
  },
  {
    property: 'width',
    copyValues: ['100px', '100%'],
  },
];
```

- [ ] localStorage에 history 저장
- [ ] navigation 클릭 시 history 저장
- [ ] 프로퍼티를 복사하면 해당 프로퍼티와 속성 값 저장

### 기능

Header

- [ ] Left-Tab이 비활성화일 때 nav 버튼 노출
- [ ] Left-Tab이 활성화일 때 nav 버튼 숨김
- [ ] nav 버튼을 누르면 Left-Tab 노출
- [ ] history 버튼을 누르면 Right-Tab 노출

Tab

- Left
  - [ ] Overlay영역 클릭 시 해당 탭 숨김
  - [ ] navigation 클릭 시 해당 css 변경
  - [ ] navigation 클릭 시 해당 프로퍼티 페이지 연결
- Right
  - [ ] 숨김 버튼 클릭 시 해당 탭 숨김
  - [ ] 확대 버튼 클릭 시 해당 탭 중앙 확대
  - [ ] history는 접근한 페이지 [+ 복사한 프로퍼티]를 출력
  - [ ] 목록에서 x/del 버튼을 누르면 해당 history 제거
  - 목록을 무한스크롤 형태로 구현
    - [ ] 목록을 최대 컴포넌트의 크기만큼 출력
    - [ ] 출력하는 history가 컴포넌트의 크기를 넘어가면 버튼 클릭 or 스크롤을 내리면 load

Main

- [ ] Box1: 프로퍼티의 간단한 설명 출력
- [ ] Box2: css 프로퍼티에 따라 필요한 input 입력으로 설정값 변경
- [ ] Screen: Box2에서 설정한 값에 따라 실시간으로 변경되는 UI 출력
- Screen의 복사 버튼 클릭 시
  - [ ] 해당 css 프로퍼티와 속성값 복사
  - [ ] window alert 메시지 출력
