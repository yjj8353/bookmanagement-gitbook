# Image

{% swagger method="get" path="/image/download" baseUrl="/api" summary="표지 다운로드" %}
{% swagger-description %}
다운로드 할 표지의 ID로 다운로드를 요청하는 API입니다.

\


인증을 필요로하지 않습니다.
{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="Long" %}
표지를 식별하기 위한 ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 지정된 표지가 다운로드됨" %}
```javascript
{
    "success": true,
    "message": null,
    "data": {
        "imageData": "data:image/<이미지포맷>;base64,<base64로 인코딩된 이미지 데이터>"
    },
    "count": 1,
    "status": "OK"
}
```
{% endswagger-response %}

{% swagger-response status="200: OK" description="정상적으로 기본 표지가 다운로드됨 (id 값이 null 이거나, 지정한 id에 해당하는 이미지 파일이 없는 경우)" %}
```javascript
{
    "success": true,
    "message": null,
    "data": {
        "imageData": "data:image/<이미지포맷>;base64,<base64로 인코딩된 이미지 데이터>"
    },
    "count": 1,
    "status": "OK"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/image/save" baseUrl="/api" summary="표지 저장" %}
{% swagger-description %}
저장할 표지 정보가 담긴 FormData 객체로 저장을 요청하는 API입니다.

\


인증을 필요로합니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="files" type="FormData" required="true" %}
표지로 사용할 이미지 데이터
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 표지가 저장됨" %}
```javascript
{
    "success": true,
    "message": "표지 저장에 성공했습니다.",
    "data": {
        "imageId": 6
    },
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
