---
layout: post
title: 2023.06.02 TIL
subtitle: Today I Learned
categories: TIL
tags: [TIL]
banner:
  image: /assets/images/til.jpeg
---

## 2023.06.02 TIL

TIL(today i learning)을 매일 써본 적이 없지만 이 기회에 루틴으로 박아두고 싶습니다. 그러나 이미 하루가 지났고 하루에 이틀치를 올릴려고 합니다.



일단 블로그를 운영 중인데 워낙 잡다한게 많아서 아마 이 블로그로 새로 시작할 것 같습니다. 욕심으로는 에드센스 붙혀서 운영하고 싶은데 내일 답변들어야 할 것 같습니다.



오늘 배운 것에 대해 하나하나 포스팅 해보겠습니다.


1. 1주차


사실 개발 언어를 python으로 시작하였고 html/css는 블로그 꾸미기 정도로만 사용해서... 이번에 제대로 개념잡고 가는 것 같습니다.



1) 웹 브라우저

기본적으로 브라우저에 요청 전송
브라우저가 받은 HTML로 구현
2) HTML & CSS

HTML은 뼈대
CSS는 꾸밈
3) HTML의 시작

VS에서 소스 코드 작성 공간 html만 적어도 html 기본 뼈대 작성 가능
4) CSS의 시작

<head> ~ </head> 안에 <style> ~ </style> 로 적습니다.
CSS는 구글링만 잘해도 가능하다는 것으로 받아들임
5) 예제들






2. 2주차


1) JavaScript

브라우저가 알아듣는 언어, 규약 같은 느낌
함수 만들어보기
function hey(){
alert('안녕!');
}
여타 언어와 비슷



2) JQuery

JavaScript의 편의 기능. 라이브러리임
단순 비교로
`document.getElementById("temp").style.display = "none";`
을

`$('#temp').hide()`


3) JavaScript & JQuery 반복문

let alphabet = ['a', 'b', 'c']
console.log(alphabet[0])
console.log(alphabet[1])
console.log(alphabet[2])
이래야 하는 것을
```java
let alphabet = ['a', 'b', 'c']
alphabet.forEach((a) => {
console.log(a)
})
```

짧게 만들었습니다.



3. 서버-클라이언트


1) 클라이언트 -> 서버: GET 요청

GET : 데이터를 조회
POST : 생성, 변경, 삭제 등 변화를 요청할


2) fetch

fetch 기본 구조
fetch("url")
.then(res => res.json())   //then은 요청 받고 할 행동 //통신 받은 데이터를 json형태로 컨트롤
.then(data => {console.log(data)}) // json으로 바뀐 데이터를 data라는 이름으로 사용


나머지는 실제 코드로 봐야함


### 2) 오늘 한 생각

이제 시작....!!!!

[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
