# 사용한 기술 스택

## 프론트엔드

### **TypeScript**/HTML5/CSS3

HTML5/CSS3는 프론트엔드를 개발할 때, 절대로 빼놓을 수 없는 요소들 입니다. TypeScript는 JavaScript가 동적 언어이기 때문에 생기는 문제를 해결하기 위해 나온 슈퍼셋(Superset: 상위 집합) 프로그래밍 언어 입니다. JavaScript와 달리 변수의 자료형을 지정할 수 있다는 점이 가장 큰 특징입니다.

### **Node.js**

자바스크립트 코드를 실행할 수 있는 런타임 어플리케이션 입니다. 이 프로젝트에서는 JavaScript 패키지 매니저인 Yarn을 설치하고 프로젝트를 빌드하는 데에 사용합니다.

### **Yarn**

Node.js를 기반으로 동작하는 npm을 대체하는 JavaScript 진영의 패키지 매니저 입니다. Java로 치면 Maven이나 Gradle과 비슷한 역할을 합니다.

### **Vue.js 3**

Vue.js 3(이하 Vue)는 SPA(Single Page Application) 프론트 엔드를 개발하는데 사용하는 프레임워크 입니다.

1.  #### **Quasar Framework**

    Vue를 기반으로 두는 UI Component 라이브러리 입니다. 디자인과 관련된 품을 줄이기 위해 사용했습니다.\

2. **Vue Router**\
   ****Vue의 공식 라우터로, 하나의 화면에서 여러 개의 페이지를 보여줄 수 있도록 도와주는 라이브러리 입니다.\
   ****
3. **Vite**\
   ****기존의 번들링 툴(Webpack 등)을 대체하는 툴 입니다. 최신 웹 브라우저들은 더 이상 번들링 과정을 필요로 하지 않기 때문에 개발 속도의 향상을 위해 사용했습니다.\
   ****
4.  #### **Pinia**

    Vue의 공식 상태 관리 라이브러리였던 Vuex를 대체하는 라이브러리 입니다. Vue의 창시자인 '에반 유'가 공식적으로 추천했던 까닭에 사용하게 되었습니다.

### **Axios**

Node.js와 브라우저를 위한 Promise 기반의 HTTP 비동기 통신 라이브러리 입니다. 일반적으로 프론트 엔드에서 백 엔드로 HTTP 요청을 할 때 사용합니다.

### **ESLint**

JavaScript 코드에서 발생할 수 있는 문제를 식별하기 위한 정적 코드 분석 도구 입니다. 문법적인 오류 뿐만 아니라, 사용자가 지정한 규칙을 기반으로 코딩 스타일의 일관성을 유지할 수 있도록 도와줍니다.

### **JSDoc**

JavaScript 기반의 문서화 도구 입니다. 또 IDE 및 텍스트 에디터에서 함수와 변수에 대한 정보를 제공할 수 있도록 도와줍니다.

## 백엔드

### Open JDK 17

백엔드 프레임워크로 스프링 부트 2를 사용했기 때문에, Java 중 가장 최신 LTS 버전인 Open JDK 17을 사용했습니다.

### **Gradle**

기존의 Ant와 Maven과 같은 빌드 도구 입니다. JVM에서 동작하는 스크립트 언어인 그루비를 기반으로 동작하기 때문에, **** 다른 빌드 도구에 비해 쉽게 익힐 수 있습니다.

### **Spring Boot 2**

스프링 부트는 기존의 스프링 프레임워크를 기반으로 하는 프로젝트 입니다. 간단한 설정으로 실행 가능한 스프링 기반의 웹 어플리케이션을 만드는 것 외에도, 자주 쓰이는 라이브러리의 호환성을 보장해 주는 것을 목표로 합니다.

1. **Spring Boot Devtools**\
   ****스프링 기반의 애플리케이션을 개발할 때 유용한 도구를 제공해주는 라이브러리 입니다.\

2. **Spring Boot Web**\
   ****스프링 MVC를 사용한 REST API 서비스를 개발하는데 사용되는 라이브러리 입니다.\
   ****
3. **Spring Data JPA**\
   ****스프링에서 JPA를 편리하게 사용할 수 있도록 도와주는 라이브러리 입니다.\

4.  #### **Spring Security**

    스프링 애플리케이션의 보안을 구현하는데 도움을 제공하는 라이브러리 입니다.

### **Java-JWT**

Java 언어에서 사용할 수 있는 JWT 생성, 파싱, 검증에 대한 도구를 제공해주는 라이브러리 입니다. Spring Security와 함께 보안을 위해 사용합니다.

### **JavaDoc**

Java 기반의 문서화 도구 입니다.

## 데이터베이스

### **PostgreSQL**

MySQL, MariaDB와 같은 오픈소스 관계형 데이터베이스 입니다. 다른 데이터베이스에 비해 표준 SQL을 잘 따르고, 점유율이 점점 증가한다는 이유 때문에 선택하게 되었습니다.

## 테스팅

### **JUnit 5**

Java 개발 시 사용하는 가장 대표적인 테스트 라이브러리 입니다. 테스트 주도 개발을 위해 사용합니다.

### Mockito

Java 개발 시 단위 테스트를 용이하게 하기 위해, 의존성이 있는 객체에 가짜 객체를 주입해주는 라이브러리 입니다.

### Postman

API 개발 시 보다 빠르고 쉽게 테스트하고 문서화 할 수 있도록 도움을 주는 애플리케이션 입니다.

## 데브옵스

### Github

대표적인 Git 버전 관리 호스팅 사이트 입니다. 프로젝트 소스 코드를 업로드하고 관리하는데 사용합니다.

### Jenkins

오픈소스로 공개된 CI/CD 도구 입니다. 자동으로 소스 코드를 테스트하고 빌드하며, 원격으로 서버에 프로젝트를 배포하는 데에 사용합니다.

### Docker

컨테이너 기반의 가상화 도구 입니다. 프로젝트 배포 시 사용되는 웹 서버 및 데이터베이스를 호스트 운영체제에 영향을 받지 않고 배포하기 위해 사용합니다.
