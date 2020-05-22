---

~~안드로이드에 fcm 전송시에는 notification를 제외하고 data만 보냄  
notification을 보내면 onMessageReceived()를 거치지 않기 때문에  
푸쉬 출력 외에 data를 받으려면 notification을 제외하고 전송해야 함~~

data와 notification을 동일하게 보내면 백그라운드, 포그라운드 모두 FCM 수신 가능

```
{
    "to": "토큰 혹은 토픽",
    "content_available": true,
    "mutable_content": true,
    "priority": "high",
    "data": {
        "title": "ttt",
        "body": "mmm",
        "image": "https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_92x30dp.png"
    },
    "data": {
        "title": "ttt",
        "body": "mmm",
        "image": "https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_92x30dp.png",
        "sound": "default",
        "badge": "1"
    },
}


```
