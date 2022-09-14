# Member

{% swagger method="post" path="/member/login" baseUrl="/api" summary="유저 로그인" %}
{% swagger-description %}
유저 로그인을 요청하는 API 입니다.

\


인증을 필요로하지 않습니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="data" type="Object" required="true" %}
username(계정)과 password(패스워드)를 담고 있는 JSON 객체.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 로그인됨" %}
새로 발급받은 Access Token, Refresh Token 값이 각각 Header의 Authorization, Authorization-refresh에 담겨 반환됨.
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="계정이 존재하지 않거나 패스워드가 틀림" %}
401 HTTP Status 외에 어떠한 데이터로 반환되지 않음.
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/member/join" baseUrl="/api" summary="새로운 유저 회원가입" %}
{% swagger-description %}
유저 회원가입을 요청하는 API 입니다.

\


인증을 필요로하지 않습니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" %}
가입요청 할 계정
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="password" %}
가입요청 할 패스워드
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="회원가입 성공" %}
```javascript
{
    "success": true,
    "message": "회원가입 성공!",
    "data": null,
    "count": 0,
    "status": "OK"
}
```
{% endswagger-response %}

{% swagger-response status="409: Conflict" description="중복된 계정 존재" %}
```javascript
{
    "success": false,
    "message": "이미 존재하는 계정명 입니다.",
    "data": null,
    "count": 0,
    "status": "CONFLICT"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/member/logout" baseUrl="/api" summary="유저 로그아웃" %}
{% swagger-description %}
유저 로그아웃을 요청하는 API 입니다.

\


인증을 필요로하지 않습니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="member" type="Object" required="true" %}
Refresh Token 값이 담긴 Member 객체
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 로그아웃됨" %}
```javascript
{
    "success": true,
    "message": "정상적으로 로그아웃 처리 되었습니다.",
    "data": null,
    "count": 0,
    "status": "OK"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/member/not-certified" baseUrl="/api" summary="인증되지 않은 유저 조회" %}
{% swagger-description %}
인증되지 않은 유저들의 정보를 요청하는 API 입니다.

\


인증을 필요로합니다.
{% endswagger-description %}

{% swagger-response status="200: OK" description="정상적으로 조회됨" %}
```javascript
// 인증되지 않은 유저가 없는 경우
{
    "success": true,
    "message": null,
    "data": [],
    "count": 0,
    "status": "OK"
}

// 인증되지 않은 유저가 하나라도 있는 경우
{
    "success": true,
    "message": null,
    "data": [
        {
            "id": <식별 가능한 고유의 ID>, 
            "name": <유저의 계정>,
            "role": <권한>
        }
    ],
    "count": 1,
    "status": "OK"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="로그인 하지 않음" %}
401 HTTP Status 외에 어떠한 데이터로 반환되지 않음.
{% endswagger-response %}

{% swagger-response status="417: Expectation Failed" description="Access Token이 유효하지 않음" %}
새로 발급받은 Access Token 값이 Header의 Authorization에 담겨 반환됨.
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/member/certify" baseUrl="/api" summary="유저 인증처리" %}
{% swagger-description %}
인증되지 않은 유저를 인증하도록 요청하는 API 입니다.

\


인증을 필요로합니다.
{% endswagger-description %}

{% swagger-parameter in="query" name="username" type="String" required="true" %}
계정
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 인증됨" %}
```javascript
{
    "success": true,
    "message": "정상적으로 인증 되었습니다.",
    "data": null,
    "count": 0,
    "status": "OK"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="로그인 하지 않음" %}
401 HTTP Status 외에 어떠한 데이터로 반환되지 않음.
{% endswagger-response %}

{% swagger-response status="417: Expectation Failed" description="Access Token이 유효하지 않음" %}
새로 발급받은 Access Token 값이 Header의 Authorization에 담겨 반환됨.
{% endswagger-response %}
{% endswagger %}
