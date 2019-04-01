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

## 예시-1

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
  console.log(item);
});
```

## 예시-2

배열을 순회하는 방법에는 여러 방법이 있는데 만들어진 순서대로 크게 `for구문`, `forEach`, `for...of` 가 있습니다.

### for

```js
const arr = [1, 2, 3];

for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

위 방식은 전통적으로 많이 쓰이던 방식이었습니다. 하지만, ES5에 forEach 메소드가 추가되고, ES2015에 for...of 구문이 추가되면서 위 방식은 잘 쓰이지 않게 되었습니다.

### forEach

```js
const arr = [1, 2, 3];

arr.forEach(item => {
  console.log(`현재 요소 ${item}에 대해 함수가 실행되고 있습니다.`);
});

arr.forEach((item, index, array) => {
  console.log(`현재 ${index + 1}번째 요소에 대해 함수가 실행되고 있습니다.`);
});
```

### for...of

```js
const arr = [1, 2, 3, 4, 5];

for (let item of arr) {
  console.log(item);
}
```

단순히 배열을 순회하기 위한 목적이라면 for...of 구문을 사용하는 것이 속도 측면에서 유리합니다. 다만, 배열을 순회하면서 배열의 인덱스가 필요한 경우에는 for...of 구문을 사용할 수 없습니다. 이 때에는 forEach 메소드를 사용하면 됩니다.

## 결론
foreach문은 for문에 비해서 더 직관적으로 코드를 작성할 수 있어 좋지만 중간에 break키워드를 사용할 수 없다는 단점이 있다. 

## 참고자료

- [MDN-foreach문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
- [helloworldjavascript-array](https://helloworldjavascript.net/pages/190-array.html)
