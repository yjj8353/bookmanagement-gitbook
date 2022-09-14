# Naver

{% swagger method="get" path="/naver-book-api/search" baseUrl="/api" summary="Naver API를 이용한 책 조회" %}
{% swagger-description %}
Naver API를 이용해 책 조회를 요청하는 API 입니다.

\


인증을 필요로합니다.
{% endswagger-description %}

{% swagger-response status="200: OK" description="정상적으로 조회됨" %}
```javascript
{
    "success": true,
    "message": null,
    "data": [
        "<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0">
    <channel>
        <title>Naver Open API - book_adv ::&apos;&apos;</title>
        <link>https://search.naver.com</link>
        <description>Naver Search Result</description>
        <lastBuildDate>Thu, 08 Sep 2022 02:29:46 +0900</lastBuildDate>
        <total>1</total>
        <start>1</start>
        <display>1</display>
        <item>
            <title>스프링 부트와 AWS로 혼자 구현하는 웹 서비스 (인텔리제이, JPA, JUnit 테스트, 그레이들)</title>
            <link>https://search.shopping.naver.com/book/catalog/32436253723</link>
            <image>https://shopping-phinf.pstatic.net/main_3243625/32436253723.20220527024357.jpg</image>
            <author>이동욱</author>
            <discount>19800</discount>
            <publisher>프리렉</publisher>
            <pubdate>20191129</pubdate>
            <isbn>9788965402602</isbn>
            <description>가장 빠르고 쉽게 웹 서비스의 모든 과정을 경험한다. 
경험이 실력이 되는 순간!

이 책은 제목 그대로 스프링 부트와 AWS로 웹 서비스를 구현합니다. JPA와 JUnit 테스트, 그레이들, 머스테치, 스프링 시큐리티를 활용한 소셜 로그인 등으로 애플리케이션을 개발하고, 뒤이어 AWS 인프라의 기본 사용법과 AWS EC2와 RDS를 사용해 서비스가 가능하도록 합니다. 이렇게 점진적으로 스프링 부트 프로젝트를 개선해서 배포 자동화하고 무중단 배포까지 경험합니다. 실무 현장에서의 노하우와 테스트 방법, 객체지향 프로그래밍 등을 소개하고 다룹니다.
 
스프링으로 하는 웹 개발이 이제는 어렵고 복잡하지 않습니다. 이 책은 기초 자바 지식만 있다면 편하게 진행할 수 있습니다. 스프링 부트 개념 설명에 집중하기 보단, 만드는 재미와 책을 보고 무엇을 만들 수 있을까에 집중했습니다. 국내 많은 서비스 회사들은 자바와 스프링을 사용하고 있습니다. 원하는 회사의 기술 스택과도 일치하고 구현하고 싶은 서비스도 쉽고 빠르게 만들고자 합니다. 전공 과제나 졸작, 취업 포트폴리오를 만들고 싶은 분들이나 실제 서비스 경험이 없는 주니어 개발자분들에게 추천합니다.</description>
        </item>
    </channel>
</rss>"
    ],
    "count": 1,
    "status": "OK"
}
```
{% endswagger-response %}

{% swagger-response status="200: OK" description="조회된 책이 없음" %}
```javascript
{
    "success": true,
    "message": "조회된 책이 없습니다",
    "data": [],
    "count": 0,
    "status": "OK"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="로그인 하지 않음" %}
401 HTTP Status 외에 어떠한 데이터로 반환되지 않음.
{% endswagger-response %}

{% swagger-response status="417: Expectation Failed" description="Access Token이 유효하지 않음" %}
 발급받은 Access Token 값이 Header의 Authorization에 담겨 반환됨.
{% endswagger-response %}
{% endswagger %}
