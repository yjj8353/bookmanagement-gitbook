# Book

{% swagger method="get" path="/book/search" baseUrl="/api" summary="책 조회" %}
{% swagger-description %}
조건을 만족하는 모든 책을 조회합니다.

\


인증을 필요로하지 않습니다.
{% endswagger-description %}

{% swagger-parameter in="query" name="title" type="" %}
책 제목
{% endswagger-parameter %}

{% swagger-parameter in="query" name="authorName" %}
저자명
{% endswagger-parameter %}

{% swagger-parameter in="query" name="publisherName" %}
출판사명
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 책 조회가 완료됨" %}
<pre class="language-json"><code class="lang-json"><strong>// 조회된 책이 한 권도 없는 경우
</strong><strong>{
</strong>    "success": true,
    "message": null,
    "data": [],
    "count": 0,
    "status": "OK"
}

// 조회된 책이 한 권 이상인 경우
// data에 책 정보가 Array 형태로 담기고, data 크기가 count에 int 형으로 담김
{
    "success": true,
    "message": null,
    "data": [
        {
            "id": 2,
            "title": "스프링 부트와 AWS로 혼자 구현하는 웹 서비스",
            "isbn": "9788965402602",
            "bookAuthorDTOs": null,
            "authors": [
                {
                    "id": 4,
                    "name": "이동욱",
                    "bookAuthorDTOs": null
                }
            ],
            "publisher": {
                "id": 3,
                "name": "프리렉",
                "bookDTOs": null
            },
            "image": {
                "id": 5,
                "name": "bookcover.jpg",
                "proxyName": "1661476700922.jpg",
                "format": "jpg",
                "path": "C:\\\\home\\retrotv\\thumnail"
            }
        }
    ],
    "count": 1,
    "status": "OK"
}</code></pre>
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/book/save" baseUrl="/api" summary="책 저장" %}
{% swagger-description %}
저장할 책 정보를 담은 Book 객체로 저장을 요청하는 API입니다.

\


인증을 필요로합니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="title" type="String" required="true" %}
책 제목
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isbn" type="String" required="true" %}
국제표준도서번호
{% endswagger-parameter %}

{% swagger-parameter in="body" name="authors" type="Array" required="true" %}
저자 정보가 담긴 Author 객체가 Array 형태로 담긴 객체
{% endswagger-parameter %}

{% swagger-parameter in="body" name="publisher" type="Object" required="true" %}
출판사 정보가 담긴 Publisher 객체
{% endswagger-parameter %}

{% swagger-parameter in="body" name="image" type="Object" required="true" %}
표지 정보가 담긴 Image 객체
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 책 저장이 완료됨" %}
```json
{
    "success": true,
    "message": "책 저장이 완료 되었습니다.",
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

{% swagger method="patch" path="/book/update" baseUrl="/api" summary="책 수정" %}
{% swagger-description %}
수정할 책 정보를 담은 Book 객체로 수정을 요청하는 API입니다.

\


인증을 필요로합니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="Long" required="true" %}
책 식별을 위해 부여되는 고유의 ID 값
{% endswagger-parameter %}

{% swagger-parameter in="body" name="title" type="String" required="true" %}
책 제목
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isbn" type="String" required="true" %}
국제표준도서번호
{% endswagger-parameter %}

{% swagger-parameter in="body" name="authors" type="Array" required="true" %}
저자 정보가 담긴 Author 객체가 Array 형태로 담긴 객체
{% endswagger-parameter %}

{% swagger-parameter in="body" name="publisher" type="Object" required="true" %}
출판사 정보가 담긴 Publisher 객체
{% endswagger-parameter %}

{% swagger-parameter in="body" name="image" type="Object" required="true" %}
표지 정보가 담긴 Image 객체
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 책 수정이 완료됨" %}
```javascript
{
    "success": true,
    "message": "책 수정이 완료 되었습니다.",
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

{% swagger method="delete" path="/book/delete" baseUrl="/api" summary="책 삭제" %}
{% swagger-description %}
삭제할 책의 ID로 삭제를 요청하는 API입니다.

\


인증을 필요로합니다.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="Long" required="true" %}
책 식별을 위해 부여되는 고유의 ID 값
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="정상적으로 책 삭제가 완료됨" %}
```javascript
{
    "success": true,
    "message": "책 삭제가 완료 되었습니다.",
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
