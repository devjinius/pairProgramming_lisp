# forEach

## 정의

forEach() 메서드는 주어진 함수를 배열 요소 각각에 대해 실행합니다.

## 함수설명

함수를 사용하는 방법은 아래와 같습니다.

`arr.forEach(callback[, thisArg]);`

- callback
  - currentValue
  - index(optional)
  - array(optional) : forEach()를 호출한 배열(arr)
- thisArg(optional) : callback을 실행할 때 this로 사용할 값입니다.

## 예시

아래 코드는 간단하게 배열을 출력하는 예시입니다.
1번 코드는 기존의 for-loop 방식이며, 2번 코드는 forEach를 사용한 방식입니다.

```js
const items = ['item1', 'item2', 'item3'];

// 1번 코드
for (let i = 0; i < items.length; i++) {
  console.log(items[i]);
}

// 2번 코드
items.forEach(function(item) {
    if (item === 'item1') {break;}
  console.log(item);
});
```

## 장단점

### 장점

### 단점

## 사용이유(정리)

## 예시

## 참고자료

[test](https://naver.com)
