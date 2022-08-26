# JWT

{% swagger method="post" path="/jwt/valid" baseUrl="/api" summary="JWT 토큰 유효성 확인" %}
{% swagger-description %}
로그인 한 유저의 JWT 토큰이 유효한지 확인하는 API 입니다.

\


유효한 경우, Access Token은 유효 여부와 관련 없이 반드시 새로 발급됩니다.

\


인증을 필요로하지 않습니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="jwt" type="Object" required="true" %}
username, accessToken, refreshToken 정보가 담긴 JSON 객체
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="토큰이 유효함" %}
새로 발급받은 Access Token 값이 Header의 Authorization에 담겨 반환됨.

```javascript
{
    "success": true,
    "message": null,
    "data": {
        "isValid": true
    },
    "count": 1,
    "status": "OK"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="토큰이 유효하지 않음" %}
```javascript
{
    "success": false,
    "message": null,
    "data": {
        "isValid": false
    },
    "count": 1,
    "status": "UNAUTHORIZED"
}
```
{% endswagger-response %}
{% endswagger %}
