---
layout: post
title: 2023.06.03 TIL
subtitle: Today I Learned
categories: TIL
tags: [TIL]
banner:
  image: /assets/images/til.jpeg
---

## 2023.06.02 TIL

일단 마지막 주차 강의를 다 듣고 마지막 예제를 하였습니다.



예제는 반복 숙달이라 비슷한 코드였고 전에 공부한 부분까지 다 합친 코드였습니다.



그러나 추가 되는것이 있는데



og 태그

<meta property="og:title" content="가수" />
    <meta property="og:description" content="응원 한마디" />
    <meta property="og:image" content="data:image/jpeg;base64" />


에 대해 배웠고 프로젝트를 AWS에 업로드하고 배포하는 것을 했는데 여기서 여러 에러를 맞아들이게 됩니다ㅋㅋㅋㅋ



일





ServiceError - Create environment operation is complete, but with errors. For more information, see troubleshooting documentation.
ServiceError - Create environment operation is complete, but with errors. For more information, see troubleshooting documentation.

이 오류..... 뭐여... 이게 뭐여 그러면서 서치를 시작했


일단 지금은 잘 작동하는데 로컬에서만 잘 작동하고 서버에서는 작동을 안하는 것입니다. 이때 mongoDB와 연결이 안된다는 것을 캐치는 했지만 chrome 검사에서


이렇게 나왔습니다. 일단 Error 500. 이게 서버의 전반적 문제라 python과  html을 뜯어봤죠

문제가 없더라구요.



두번째 JSON인식 불가.

하..... 이게 잘못 판단한게 JavaScript와 JSON의 비교 인식을 잘못해서 그런거라고 생각했습니다.

이제 여기서부터 희대의 삽질이 시작됩니다ㅋㅋ



스파르타에서 제공하는 소스 코드로 다시 해보기. AWS 초기화 등등 많은 것을 해보았다. 바로 물어보려고 했으나 이미 새벽시간. 홀리..... 그러면서 JSON 역직렬화를 하면 데이터 문자열을 객체로 변환하여 JSON 인식 불가를 해결하셨다는 글을 보고

const json = JSON.parse( content );
그런데 애초에 JavaScript object 아닌가.. 역시나 해결점이 아니다.

그래서 돌아돌아 다시 mongoDB를 주목했다. 역시... 에러도 중요하지만 어디서 문제가 생겼는지 파악하는게 먼저였습니다. 분명 save_comment 부분부터 작동을 안하면 db문제를 확인했어야 했는데 error에 속아 돌고 돌았으니...



결론은 AWS에서 mongoDB로 access가 안되는 것인데 보니까 전체 접속 권한이 없었다... 그래서



![다운로드 (1).png](/assets/images/post/1.png)
![다운로드.png](/assets/images/post/2.png)


access 접근 가능한 `0.0.0.0/0` 을 입력해주고 나서 해결했다!!!!! 물론 삽질은 삽질이지만 이를 통해서 코드를 한 20번은 봤고 하나하나 길을 따라가며 작동원리에 대해 깊은 고찰을 하는 계기가 되었다.


### 2) 오늘 한 생각

오류 해결시 쾌감 쩐다

[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
