---
layout: post
title: 2023.06.02 TIL2
subtitle: Today I Learned
categories: TIL
tags: [TIL]
banner:
  image: /assets/images/til.jpeg
---

## 2023.06.02 TIL
파이썬!! 가볍게 문법과 패키지 설치는 넘아가겠습니다. 자신 있어서 그런건 아니고 사용은 해봤으니까 넘어가겠습니다.

그러나 git bash에서 있었던 가상환경 생성 오류가 있어 포스팅 따로 붙혀놓겠습니다.

1. 3주차


네이버 증권에서 데이터 받아온 적 있는데 몇년 전이라 가물가물 하던걸 다시 상기하는 좋은 기회였습니다.



1) 크롤링을 위한 beautiful soup4 패키지 설치!



beautiful soup는 크롤링을 위한 패키지입니다. requests 모듈을 통해 요청을 보내고 받아오는 형태의 라이브러리

html, xml 파일로 데이터를 파싱하는 라이브러리

bs4로 명명합니다.



2) 크롤링하기


이런 식으로 chrome에서 오른쪽 마우스->검사를 통해 개발자보드로 들어감

기본 셋팅은

import requests
from bs4 import BeautifulSoup

URL = "https://movie.daum.net/ranking/reservation"
headers = {'User-Agent' : 'Mozilla/5.0 (Windows NT 10.0; Win64; x64)AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.86 Safari/537.36'}
data = requests.get(URL,headers=headers)
soup = BeautifulSoup(data.text, 'html.parser')




3) mongoDB



여러 DB의 형태가 있겠지만 mongoDB를 사용.

간단히 말하면



찾기 쉽게 저장.



# 저장 - 예시
doc = {'name':'bobby','age':21}
db.users.insert_one(doc)

# 한 개 찾기 - 예시
user = db.users.find_one({'name':'bobby'})

# 여러개 찾기 - 예시 ( _id 값은 제외하고 출력)
all_users = list(db.users.find({},{'_id':False}))

# 바꾸기 - 예시
db.users.update_one({'name':'bobby'},{'$set':{'age':19}})

# 지우기 - 예시
db.users.delete_one({'name':'bobby'})
알고 있자




2. 4주차


1) Flask



가상환경 만들고 Flask 패키지 설치하고 실행하면 사이트 나옴



http://localhost:5000



그다음 예시 계속 함



2) frontend & backend



app.py와 idex.html 준비하시고

서버 코드로

@app.route('/')
def home():
return render_template('index.html')

@app.route('/test', methods=['POST'])
def test_post():
title_receive = request.form['title_give']
print(title_receive)
return jsonify({'result':'success', 'msg': '이 요청은 POST!'})

클라이언트로

function hey() {
let formData = new FormData();
formData.append("title_give", "블랙팬서");
```javascript
{
    fetch("/test", {method: "POST", body: formData}).then(res => res.json()).then(data => {
        console.log(data)
    })
}

```
            


html에 <body></body>에서 버튼을 눌렀을 때 hey()가 발동



그럼 "title_give" 와 블랙팬서가 포함된 폼필드 생성.



<input name="title_give" value="블랙팬서">

라고 보면 됨. 이 formdata를 fetch로 폼데이터를 전송할 수 있는데 이 때 json형태가 아닌 formdata 타입으로 맞추어야함.

body:formData 이 부분이 body 부분에 폼데이터를 할당함.



python 파일에서는



decoration route는 url이 요청이 들어왔을 때 함수 호출



/test 요청이 들어오면 title_receive 함수에 title_give 폼데이터를 저장하고

response로 success와 메세지



밑에 예제도 비슷한대 완전 정리되면 올리겠습니다.



### 2) 오늘 한 생각

은근 복잡하다

[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
