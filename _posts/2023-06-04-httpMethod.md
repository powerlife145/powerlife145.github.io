---
layout: post
title: Http Method
subtitle: Http Method의 설명과 종류
categories: Python
tags: [database]
banner:
  image: https://www.w3big.com/redis/pubsub2.png
---
## HTTP method



### 1.  HTTP 프로토콜

HTTP(HyperText Transfer Protocol)는 월드 와이드 웹에서 데이터를 전송하는 프로토콜입니다. 웹 브라우저(클라이언트)와 웹 서버 간의 통신 규약을 정의합니다. HTTP는 일반적으로 HTML 문서, 이미지, 비디오, JSON, XML 등 다양한 유형의 리소스를 전송하는 데 사용됩니다.

말하자면 통신 규약을 중심으로 요청이나 응답을 반환을 진행하게 됩니다. 여기서 POST & GET에 대해 설명하면



### 2. HTTP 메서드

HTTP는 다양한 메서드(GET, POST, PUT, DELETE 등)를 지원합니다. 이 메서드들은 클라이언트가 웹 리소스에 수행하려는 작업을 서버에 알려주기 위한 방법입니다.

- **GET**: 서버로부터 데이터를 조회(요청)합니다. (쉽게 설명하면 가져옵니다.)
- **POST**: 서버에 새로운 데이터를 생성하거나 보냅니다. (쉽게 설명하면 보냅니다.)
- **PUT**: 서버의 특정 리소스를 수정합니다. (쉽게 설명하면 수정합니다.)
- **DELETE**: 서버의 특정 리소스를 삭제합니다. (쉽게 설명하면 삭젱합니다.)
-



### 3. HTTP 상태 코드

HTTP 응답에는 상태 코드(status code)가 포함되어 있어, 요청이 성공적으로 처리되었는지, 오류가 발생했는지 등을 나타냅니다.

- `2xx`: 성공 (예: 200 OK)
- `3xx`: 리다이렉션 (예: 301 Moved Permanently)
- `4xx`: 클라이언트 오류 (예: 404 Not Found)
- `5xx`: 서버 오류 (예: 500 Internal Server Error)



### 예시 )

#### 1) GET

```python
import requests

response = requests.get('http://example.com/data?id=1')
if response.status_code == 200:
    print(response.text)

```

- `GET` 메서드는 서버로부터 정보를 요청하기 위해 사용됩니다.
- `GET` 요청은 URL에 모든 데이터를 포함합니다. 예를 들어, `http://example.com/data?id=1`
- `GET`은 브라우저 히스토리에 기록되며, 북마크도 가능합니다.
- 보안이 필요한 데이터에는 적합하지 않습니다(패스워드 등).



#### 2) POST

```python
import requests

data = {'id': 1, 'name': 'John'}
response = requests.post('http://example.com/data', data=data)
if response.status_code == 200:
    print(response.text)
```

- `POST` 메서드는 서버로 데이터를 보내기 위해 사용됩니다.
- 데이터는 요청 본문에 포함되어 있습니다, 따라서 보안이 더 강화됩니다.
- `POST`는 브라우저 히스토리에 기록되지 않고, 북마크도 할 수 없습니다.
- 대량의 데이터를 보낼 수 있습니다.



이렇게 POST 나 GET을 적절하게 사용하여 효과적인 웹 어플리케이션을 만들 수 있습니다.




[1]: https://daringfireball.net/projects/markdown/
  [2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
  [3]: https://www.markitdown.net/
  [4]: https://daringfireball.net/projects/markdown/basics
  [5]: https://daringfireball.net/projects/markdown/syntax
