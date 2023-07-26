# ✨ 자바스크립트 밴딩머신 기능 구현 ✨

## [👉 밴딩머신 링크](https://skyllerrr.github.io/Vending_Machine/)

## 🔥 구현 목표 🔥

1. 소지금 내에서 입금하기
2. 입금한 돈으로 음료 구매하기
3. 구매하고 남은 거스름돈 받기
4. 선택, 획득한 아이템 목록 표시하기
5. 재고에 따라 메뉴버튼 사용 가능 여부 변경하기
6. 한번으로 끝나지 않는 프로그램 만들기
7. 최초 소지금, 상품 추가, 재고 관리 쉽게 하기
8. 여러 상황에 따라 유효성 확인 및 안내 띄우기

    - 입금할 금액보다 소지금이 부족할 때
    - 입금액이 상품 총액보다 부족할 때
    - 1000원 단위 입금이 아닐 때
    - 구매하려는 아이템이 재고가 없을 때
    - 거스름돈 안내, 아이템 선택 중에 거스름돈을 받으려고 할 때

---

## 🔥 기능 🔥

-   상품 목록 생성
-   소지금 계산, 표시
-   입금, 잔액 표시
-   거스름돈 계산, 표시
-   선택 아이템 목록 추가, 개수 누적, 선택 삭제
-   획득시 획득 목록 추가, 개수 누적
-   획득시 총 금액 계산, 표시

---

## 🔥 기능 분리하기 🔥

-   `init`
-   `getter`, `setter`
-   `calculation`
-   `function`
-   `validation`
-   `reset`

---

## 🔥 알아보기 🔥

-   `console.log()` 로 내가 원하는 정보 확인하기
-   `alert()` 로 내가 원하는 알림 띄우기
-   `let`, `const`
    -   변하는 값, 변하지 않는 값 구분하기
-   `for` 와 `forEach()`
    -   반복과 순회
    -   for, forEach()의 차이
        -   for문은 동기, forEach() 함수(내장)는 비동기 방식
            -   동기 : 요청, 결과가 동시에 이루어짐(시작 -> 끝 -> 시작 -> 끝)
            -   비동기 : 요청, 결과가 동시에 이루어지지 않음(시작 시작 끝 시작 끝 끝)
        -   for문은 원하는 정보에 접근하기 쉬움, forEach()는 어려움
        -   for문은 반복 횟수를 정해줘야하지만 forEach()는 알아서 처음부터 끝까지 하나씩 순회
    -   forEach(), callback 함수
-   `if ~ else if, else`
    -   else와 else if : 명확한 조건 설정
-   `document`
    -   .querySelector(), .querySelectorAll()
        -   id, class, selector, element
    -   .getElementById()
        -   id
    -   .getElementsByTagName()
        -   element
    -   .createElement()
        -   setAttribute()
        -   appendChild()
        -   removeChild()
-   `list` 로 아이템 목록 만들고 활용하기
-   `Map`
    -   아이템 정보 활용하기
    -   get, set으로 값 변경하기
-   `function` 으로 원하는 기능 구현하기
    -   작은 기능부터 구현하기
    -   매개변수 써먹기
    -   `=>` 화살표 함수
-   `addEventListener()` 로 이벤트 추가하기
-   `｀${}｀` 로 원하는 값 대입하기
-   `insertAdjacentHTML`, `insertAdjacentTEXT`
    -   innerHTML, innerTEXT, textContent, DOM 구조
        -   inner~ 는 element의 내용을 `변경`할때 사용
            -   변경할 내용 파싱 -> 변경 내용 파싱하여 객체 생성 -> 객체 대입
        -   insertAdjacent~ 는 element 내용을 `삽입`할때 사용
            -   변경 내용 파싱하여 객체 생성 -> 객체 대입
        -   왜 textContent?
            -   innerText는 사람이 읽을 수 있는 내용만, 리플로우 발생
            -   innerHTML은 HTML을 분석, textContent는 raw text
            -   textContent는 노드의 모든 요소 반환, XSS 공격 위험 없음
            -   [XSS공격](https://nordvpn.com/ko/blog/xss-attack/)
