[Welcome Page](https://iamodh.github.io/welcome-page/)
=

> PC

![welcome-page-pc](https://github.com/iamodh/welcome-page/assets/68431235/accc657b-685a-43f1-a93c-adc17fea82b8)

> Mobile

![welcome-page-mobile](https://github.com/iamodh/welcome-page/assets/68431235/5de33bbd-1ddc-4aee-a754-c6bb35d0fd7a)

## Table of Contents
- [Built with](#built-with)
- [Project](#project)
- [Features](#features)

## Built with
### Front-end
- `HTML`
- `CSS`
- `JavaScript`

## project    
> 1. 배경 이미지 변경
- `position.coords`를 이용해 유저의 `latitude`와 `longitude`를 받습니다.
- `Openweathermap API`를 이용해 해당 지역의 온도와 날씨를 받습니다.
- 알맞은 배경 이미지를 `img`폴더에서 불러옵니다.

> 2. 로그인
- `localstorage`에 저장된 `userName` Key로부터 value를 불러와 화면에 표시합니다.
- `savedUserName`이 `null`이라면 `loginForm`이 표시되고 유저의 입력을 value로 저장합니다.

> 3. to-do list
- list 작성 후 제출 시 `Date.now()` 값을 id로 부여받은 `newTodoObj가 `todos` 배열에 저장됩니다.
- 동시에 `localStorage`의 `todos` key에 배열이 json 형태로 저장되고 화면에 list가 출력됩니다.
- 삭제 버튼 클릭 시 해당 element가 화면에서 지워지고 filter 함수를 통해 `localStorage`에서도 수정됩니다.

```Javascript
// 함수 결과가 true인 element들을 제거한다.
todos = todos.filter((todo) => todo.id !== parseInt(li.id));
```

> 4. Clock
- 현재 시간을 받는 `getClock` 함수를 `setInterval`을 통해 1초에 1회씩 실행한다.
- `getClock` 안의 `rotateHands` 함수는 현재 시간에 해당하는 각도 만큼 시침과 분침을 회전한다.

```Javascript
// rotate clock hands along the time
function rotateHands(date) {
  const hourRotation = 360 * ((date.getHours() % 12) / 12);
  const minuteRotation = 360 * (date.getMinutes() / 60);

  hourHand.style.transform = `rotate(${hourRotation}deg)`;
  minuteHand.style.transform = `rotate(${minuteRotation}deg)`;
}
```

## Features
- [x] Login
- [x] To-do list
- [x] Weather & Temperature
- [x] Clock

