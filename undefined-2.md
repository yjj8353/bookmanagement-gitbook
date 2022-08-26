# 사용한 기술 스택

## 프론트 엔드

1.  **Node.js**

    자바스크립트 코드를 실행할 수 있는 런타임 어플리케이션 입니다. 이 프로젝트에서는 JavaScript 패키지 매니저인 Yarn을 설치하고 프로젝트를 빌드하는 데에 사용합니다.\

2.  **Yarn**

    Node.js를 기반으로 동작하는 JavaScript 진영의 패키지 매니저 입니다. Java로 치면 Maven이나 Gradle과 비슷한 역할을 합니다.\

3.  **Vue.js 3**

    Vue.js 3(이하 Vue)는 SPA(Single Page Application) 프론트 엔드를 개발하는데 사용하는 프레임워크 입니다. \


    1.  **Quasar Framework**

        Vue를 기반으로 두는 UI Component 라이브러리 입니다. 디자인과 관련된 품을 줄이기 위해 사용했습니다.\

    2. **Vue Router**\
       ****Vue의 공식 라우터로, 하나의 화면에서 여러 개의 페이지를 보여줄 수 있도 도와주는 라이브러리 입니다.\

    3. **Vite**\
       ****기존의 번들링 툴(Webpack 등)을 대체하는 툴 입니다. 최신 웹 브라우저들은는 더 이상 번들링 과정을 필요로 하지 않기 때문에 개발 속도의 향상을 위해 사용했습니다.\
       ****
    4. **Pinia**\
       ****Vue의 공식 상태 관리 라이브러리였던 Vuex를 대체하는 라이브러리 입니다. Vue의 창시자인 '에반 유'가 공식적으로 추천했던 까닭에 사용하게 되었습니다.\
       ****
4. **TypeScript**\
   ****TypeScript는 JavaScript가 동적 언어이기 때문에 생기는 문제를 해결하기 위해 나온 슈퍼셋(Superset: 상위 집합) 프로그래밍 언어 입니다. JavaScript와 달리 변수의 자료형을 지정할 수 있다는 점이 가장 큰 특징입니다.\
   ****
5. **Axios**\
   ****Node.js와 브라우저를 위한 Promise 기반의 HTTP 비동기 통신 라이브러 입니다. 일반적으로 프론트 엔드에서 백 엔드로 HTTP 요청을 할 때 사용합니다.\
   ****
6. **ESLint**\
   ****JavaScript 코드에서 발생할 수 있는 문제를 식별하기 위한 정적 코드 분석 도구 입니다. 문법적인 오류 뿐만 아니라, 사용자가 지정한 규칙을 기반으로 코딩 스타일의 일관성을 유지할 수 있도록 도와줍니다.\

7. **JSDoc**\
   ****JavaScript 기반의 문서화 도구 입니다. 또 IDE 및 텍스트 에디터에서 함수와 변수에 대한 정보를 제공할 수 있도록 도와줍니다.

## 백 엔드

1. **Gradle**
2. **Spring Boot 2**
   1. **Spring Boot Devtools**
   2. **Spring Boot Web**
   3. **Spring Data JPA**
   4. **Spring Security**
3. **Java-JWT**
4. **ModelMapper**
5. **Jackson**
6. **Lombok**
7. **JUnit 5**
8. **JavaDoc**

## 데이터베이스

PostgreSQL
