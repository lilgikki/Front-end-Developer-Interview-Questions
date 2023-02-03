*Вопрос: Чему равно `foo`?*
```javascript
var foo = 10 + '20';
```

**Ответ: ```1020``` При сложении числа и строки происходит конкатенация**

*Вопрос: Что выводит код ниже?*
```javascript
console.log(0.1 + 0.2 == 0.3);
```

**Ответ: ```false```. Это особенность машинного вычисления и плавающей точки **

*Вопрос: Как сделать, чтобы это выражение работало?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

**Ответ:**
```javascript
const add = (a, b) => {
  if (a&&b) {
    return a + b;
  } else {
    return (c) => {return a + c;};
  }
};
```

*Вопрос: Какое значение возвращает данное выражение?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

**Ответ: ```goh angasal a m'i```. Строка разбивается на массив, переворачивается и соединяется снова в строку.**

*Вопрос: Чему равно `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```

**Ответ:**

*Вопрос: Что покажут эти два alert?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

**Ответ: ```ReferenceError: bar is not defined``` т.к. переменная bar определена внутри функции.**

*Вопрос: Чему равно `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

**Ответ: 2.

*Вопрос: Чему равно `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

**Ответ: ```undefined```. Так как в момент определеня ```foo.x``` ```foo``` перезаписывается на новое значение.**

*Вопрос: Что выводит код ниже?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

**Ответ: ```one three two``` Так как ```SetTimeout``` часть основной очереди**

*Вопрос: В чем разница между этими четырьмя промисами (promises)?*
```javascript
doSomething().then(function () {
  return doSomethingElse();
});

doSomething().then(function () {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```

**Ответ:**
