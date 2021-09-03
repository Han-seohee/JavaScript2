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

---
### :star2:배열 내장함수 forEach

```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];

for (let i = 0; 1 < superheroes.length; i++) {
 console.log(superheroes[i]);
}

// 값 : 아이언맨
        캡틴 아메리카
        토르
        닥터 스트레인지
```

:point_down: forEach

```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];

function print(hero) {
 console.log(hero);
}

superheroes.forEach(print)

// 값 : 아이언맨
        캡틴 아메리카
        토르
        닥터 스트레인지
```

:point_down: 짧은 코드로

```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];

superheroes.forEach(function(hero) {
 console.log(hero);
});

// 값 : 아이언맨
        캡틴 아메리카
        토르
        닥터 스트레인지
```

:point_down: 화살표 함수로 

```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];

superheroes.forEach(hero => {
 console.log(hero);
});

// 값 : 아이언맨
        캡틴 아메리카
        토르
        닥터 스트레인지
```

---
2021.09.03

### :star2:배열 내장함수 map

>for문

```
const array = [1, 2, 3, 4, 5, 6, 7, 8];

const squared = [];
for (let i = 0; i < array.length; i++) {
 squared push(array[i] * array[i]);
}

console.log(squared);

// 값 : [1, 4, 16, 25, 36, 49, 64]
```

>forEach문

```
const array = [1, 2, 3, 4, 5, 6, 7, 8];

const squared = [];
array.forEach(n => {
 squared.push(n *n);
});

console.log(squared);

// 값 : [1, 4, 16, 25, 36, 49, 64]
```

>map
>>배열의 내용에 전체적으로 변환을 주고 싶을 때

```
const array = [1, 2, 3, 4, 5, 6, 7, 8];

const square = n => n * n;
const squared = array.map(square);

// 값 : [1, 4, 16, 25, 36, 49, 64]
```

```
const array = [1, 2, 3, 4, 5, 6, 7, 8];

const squared = array.map(n => n * n);

// 값 : [1, 4, 16, 25, 36, 49, 64]
```

>활용
>>텍스트로만 이루어진 문자열로 바꾸기

```
const items = [
 {
   id: 1,
   text: 'hello'
 },
 {
   id: 2,
   text: 'bye'
 }
];

const texts = items.map(item => item.text);
console.log(texts);

// 값 : ["hello", "bye"]
```

#### :star:배열에서 원하는 항목이 어디에 있는지 알려주는 함수

>index of
>>특정 값과 일치하는것을 찾을 때

```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];
const index = superheroes.indexOf('토르');
console.log(index);

// 값 : 2
```

>findIndex
>>특정 값을 조건으로 찾아서 몇번째인지 찾기

```
const todos = [
 {
   id: 1,
   text: '자바스크립트 입문',
   done: true,
 },
 {
   id: 2,
   text: '함수 배우기',
   done: true,
 },
 {
   id: 3,
   text: '객체와 배열 배우기',
   done: true,
 },
 {
   id: 4,
   text: '배열 내장함수 배우기',
   done: false,
 }
]

const index = todos.findIndex(todo => todo.id === 3)
console.log(index);

// 값 : 2
```

>find
>>찾은 값 자체를 반환

```
const todos = [
 {
   id: 1,
   text: '자바스크립트 입문',
   done: true,
 },
 {
   id: 2,
   text: '함수 배우기',
   done: true,
 },
 {
   id: 3,
   text: '객체와 배열 배우기',
   done: true,
 },
 {
   id: 4,
   text: '배열 내장함수 배우기',
   done: false,
 }
]

const todo = todos.find(todo => todo.done === false)
console.log(todo);

// 값 : Object {id: 4, text: "배열 내장함수 배우기", done: false}
```

---

### :star2:배열 내장함수 filter

특정 조건을 만족하는 원소를 찾아서 새로운 배열을 만드는 것

```
const todos = [
 {
   id: 1,
   text: '자바스크립트 입문',
   done: true,
 },
 {
   id: 2,
   text: '함수 배우기',
   done: true,
 },
 {
   id: 3,
   text: '객체와 배열 배우기',
   done: true,
 },
 {
   id: 4,
   text: '배열 내장함수 배우기',
   done: false,
 }
]

const tasksNotDone = todos.filter(todo => todo.done === false);
// 간단히 const tasksNotDone = todos.filter(todo => !todo.done);
console.log(taskNotDone);

// 값 : [Object]
         0: Object
          id: 4
          text: "배열 내장함수 배우기"
          done: false
```

```
const todos = [
 {
   id: 1,
   text: '자바스크립트 입문',
   done: true,
 },
 {
   id: 2,
   text: '함수 배우기',
   done: true,
 },
 {
   id: 3,
   text: '객체와 배열 배우기',
   done: true,
 },
 {
   id: 4,
   text: '배열 내장함수 배우기',
   done: false,
 }
]

const tasksNotDone = todos.filter(todo => todo.done === true);
// 간단히 const tasksNotDone = todos.filter(todo => todo.done);
console.log(taskNotDone);

// 값 : [Object, Object, Object]
         0: Object
          id: 1
          text: "배열 내장함수 배우기"
          done: true
         1: Object
          id: 2
          text: "함수 배우기"
          done: true
         ...(done값이 true인것만)
```

---

### :star2:배열 내장함수 splice와 slice

>splice
>>배열에서 특정 항목을 제거할 때 사용
>>제거하는 과정에서 해당 원소가 몇번 째 인지 명시를 해야함 

```
const numbers = [10, 20, 30, 40];
const index = numbers.indexOf(30);
numbers.splice(index, 1);
console.log(numbers);

// 값 : [10, 20, 40]
```

```
const numbers = [10, 20, 30, 40];
const index = numbers.indexOf(30);
const spliced = numbers.splice(index, 1);
console.log(spliced);
console.log(numbers);

// 값 : [30]
        [10, 20, 40]
```

```
const numbers = [10, 20, 30, 40];
const index = numbers.indexOf(30);
const spliced = numbers.splice(index, 2);
console.log(spliced);
console.log(numbers);

// 값 : [30, 40]
        [10, 20]
```

>slice
>>배열을 잘라낼 때 사용
>>기존의 배열을 건들이지 않음

```
const numbers = [10, 20, 30, 40];

const sliced = numbers.slice(0, 2);     //0부터 2 전까지니까 10, 20
console.log(sliced);
console.log(numbers);

// 값 : [10, 20]
        [10, 20, 30, 40]
```

---
### :star2:배열 내장함수 shift, pop, unshift, push

>shift
>>기존의 배열을 수정
>>첫번째 원소를 배열에서 추출

```
const numbers = [10, 20, 30, 40];

const value = numbers.shift();
console.log(value);
console.log(numbers);

// 값 : 10
        [20, 30, 40]  //numbers.shift() 쓸 때마다 왼쪽부터 하나씩 빠짐
```

```
const numbers = [10, 20, 30, 40];

const value = numbers.shift();
numbers.shift()
numbers.shift()
numbers.shift()
console.log(value);
console.log(numbers);

// 값 : 10
        []
```

>pop

```
const numbers = [10, 20, 30, 40];

const value = numbers.pop();
console.log(value);
console.log(numbers);

// 값 : 40
        [10, 20, 30]   //numbers.pop() 쓸 때마다 오른쪽부터 하나씩 빠짐
```

>unshift

```
const numbers = [10, 20, 30, 40];
numbers.nushift(5);
console.log(numbers);

// 값 : [5, 10, 20, 30, 40]     // 앞쪽에 5를 추가
```

>concat
>>배열 합치기
>>기존의 배열을 건들이지 않음

```
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const concated = arr1.concat(arr2);
console.log(arr1);
console.log(arr2);
console.log(concated);

// 값 : [1, 2, 3]
        [4, 5, 6]
        [1, 2, 3, 4, 5, 6]
```

```
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const concated = [...arr1, ...arr2];
console.log(concated);

// 값 : [1, 2, 3, 4, 5, 6]
```

>join
>>배열 안에 있는 값들을 문자열 형태로 합칠 때

```
const array = [1, 2, 3, 4, 5];
console.log(array.join());
console.log(array.join(' '));
console.log(array.join(', '));

// 값 :  1,2,3,4,5
         1 2 3 4 5
         1, 2, 3, 4, 5
```

---

### :star2:배열 내장함수 reduce

```
const numbers = [1, 2, 3, 4, 5];

let sum = 0;
numbers.forEach(n => {
  sum += n;
});

console.log(sum);

// 값 : 15
```
>배열의 합 구하기

<img src="https://user-images.githubusercontent.com/86407453/132000667-d8bfb9fa-1730-4926-aaf1-050b1fa234b3.png">

```
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, current) => accumulator + current, 0);
console.log(sum);

// 값 : 15
```

>배열의 평균 구하기

```
const numbers = [1, 2, 3, 4, 5];

const avg = numbers.reduce((accumulator, current, index, array) => {
 if (index === array.length - 1) {
  return (accumulator + current) / array.length;
 }
 return accumulator + current;
}, 0);
console.log(avg);

// 값 : 3
```

---
### :star2:배열 내장함수 reduce
>다른예시

```
const alphabets = ['a', 'a', 'a', 'b', 'c', 'c', 'd', 'e'];
const counts = alphabets.reduce((acc, current) = > {
 if (acc[current]) {
  acc[current] += 1;
 } else {
   acc[current] = 1;
 }
 return acc;
}, {})

console.log(counts); 

// 값 : Object {a: 3, b: 1, c: 2, d: 1, e: 1}
```
