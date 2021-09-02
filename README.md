# JavaScript 자바스크립트 이론2
2021.09.02
### :star2:배열

```
const array = [1, 2, 3, 4, 5];
console.log(array);

// 값 : [1, 2, 3, 4, 5] 
```

```
const array = [1, 'blabla', {}, 4];
console.log(array[0]);

// 값 : [1] 

const array = [1, 'blabla', {}, 4];
console.log(array[1]);

// 값 : [blabla] 
```

```
const objects = [
 { name : '멍멍이' },
 { name : '야옹이' }
];

console.log(object);
console.log(object[0]);
console.log(object[1]);

//값 : [Object, Object]
        Object {name: "멍멍이"}
        Object {name: "야옹이"} 
```

>새로운 항목 추가하기

```
const objects = [
 { name : '멍멍이' },
 { name : '야옹이' }
];

objects.push ({
 name: '멍뭉이'
});

console.log(objects);

// 값 : [Object, Object, Object]
         0: Object
         1: Object
         2: Object
            name: "멍뭉이"
```

>배열의 크기 알아내기

```
const objects = [
 { name : '멍멍이' },
 { name : '야옹이' }
];

console.log(objects.length);

objects.push ({
 name: '멍뭉이'
});

console.log(objects.length);

// 값 : 2
        3
```
>복습

```
const array = [1, true, {a: 1}, [1,2,3,4]];
array.push(6); //추가

//추가
console.log(array)
//크기
console.log(array.length)

//조회
console.log(array[0])
console.log(array[1])
console.log(array[2])
console.log(array[3])
console.log(array[4])
```

---
### :star2:반복문 for

>for

```
for (let i = 0; i < 10; i++) {
 console.log(i);
}

// 값 : 0
        1
        2
        ...
        9
```

```
for (let i = 10; i > 0; i--) {
 console.log(i);
}

// 값 : 10
        9
        8
        7
        ...
        1
```

```
for (let i = 10; i >= 0; i-=2) {
 console.log(i);
}

// 값 : 10
        8
        6
        ...
        0
```

>for문과 배열

```
const names = ['멍멍이', '야옹이', '멍뭉이'];

for (let i= 0; i < names.length; i++) {
 console.log(names[i]);
}

// 값 : 멍멍이
        야옹이
        멍뭉이
```

---
### :star2:반복문 while

```
let i = 0;

while(i < 10) {
 console.log(i);
 i++;
}
```

```
let i = 0;
let isFun = false;

while (isFun === false) {
 console.log(i);
 i++;
 if (i === 30) {
  isFun = true;
 }
}

// 값 : 0
        1
        ...
        29
```

```
let i = 0;
let isFun = false;

while (!isFun) {
 console.log(i);
 i++;
 if (i === 30) {
  isFun = true;
 }
}

// 값 : 0
        1
        ...
        29
```

---
### :star2:반복문 for...of, for...in

>for...of - 배열 안에 있는것들을 사용해서 어떠한 작업을 할 때

```
const numbers = [10, 20, 30, 40, 50];

for (let number of numbers) {
 console.log(numbers);
}

// 값 : 10
        20
        ...
        50
```
>객체의 정보를 받아올수 있는 몇가지 방법

```
const numbers = [10, 20, 30, 40, 50];

const doggy = {
 name: '멍멍이',
 sound: '멍멍',
 age: 2
};

console.log(Object.entries(doggy));
console.log(Object.keys(doggy));
console.log(Object.values(doggy));

// 값 : (key+value)
        ["name", "sound", "age"]
        ["멍멍이", "멍멍", 2] 
```

>for...in - 객체에 대한 반복적인 작업을 처리할 때 

```
const doggy = {
 name: '멍멍이',
 sound: '멍멍',
 age: 2
};

for (let key in doggy) {
 console.log(`${key}; ${doggy}`);
}

// 값 : name: 멍멍이
        sound: 멍멍
        age: 2
```

---
### :star2:반복문 continue, break
반복문에서 벗어나거나 그 다음 루프를 돌게 할 수 있다.

>countinue

```
for (let i = 0; i < 10; i ++) {
 if (i === 2) continue;     // 특정 조건이 만족됐을 때 그 다음 루프 실행
 console.log(i);     // 스킵됨
}

// 값 : 0
        1
        3
        4
        ...
        9
```

>break

```
for (let i = 0; i < 10; i ++) {
 if (i === 2) continue;
 console.log(i);
 if (i === 5) break;     // 반복문이 끝남

// 값 : 0
        1
        3
        4
        5
```
