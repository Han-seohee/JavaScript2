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
