---
layout : post
title : "엔트리 개발"
---
# entry js
<hr>
자바스크립트 기반으로 엔트리에서 보여지는 블록들을 정의하고, 핀번호나 아두이노에 필요한 value 데이터를 **sendQeue**에 담아서 entry-hw로 전송한다. 반대로 아두이노의 센서값을 읽어와서 블록에 반환할 수 있다. 패킷은 자유롭게 작성 가능하나 key,value의 **리스트 형식**을 추천하고 있다.

## block_mindpiggy.js
entryjs에서는 하드웨어 개발시 이 파일만 작성하면 된다. 엔트리에서 개발하기 쉽도록 필수 메소드들을 정의해 놨고, Entry-Docs에서 안내해주는 형식에 맞춰 채워넣기만 하면 된다. 다음은 mindpiggy 각 메소드의 코드 해석이다.

1. Entry.Mindpiggy
    
``` js 
PORT_MAP: {
    //코드 내 전역변수
    digitalpin:0,
    moodneopixel:[12,0,0,0],
    chipneopixel:[0,0,0],
    vibration:0,
    soundsensor:0,
    photointerrupt:0,
    speaker:[0,0],
},
```
    
~~데이터를 초기화 해주기 위한 변수. Entry.Mindpiggy.PORT_MAP._key_ 로 접근가능하다.~~ 스피커의 주파수 초기화 문제로 PORT_MAP을 사용하지않고 초기화하게 수정함.

```js
id: '29.1',
name: 'Mindpiggy',
url: 'http://inuscoop.com',
imageName: 'mindpiggy.png',
title: {
    "en": 'mindpiggy',
    "ko": '마인드피기'
},
```
    
    