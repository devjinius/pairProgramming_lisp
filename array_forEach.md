# forEach

## 정의
forEach() 메서드는 주어진 함수를 배열 요소 각각에 대해 실행합니다.

## 함수설명
`
arr.forEach(callback[, thisArg]);
`
- callback
    - currentValue
    - index 
    - Array : forEach()를 호출한 배열.

- thisArg : callback을 실행할 때 this로 사용할 값.

## 간단예시
```js
const items = ['item1', 'item2', 'item3'];
const copy = [];

// 이전
for (let i=0; i<items.length; i++) {
  copy.push(items[i]);
}

// 이후
items.forEach(function(item){
  copy.push(item);
});
```

## 장단점




### 장점

### 단점

## 사용이유(정리)

## 예시

## 참고자료

[test](https://naver.com)
