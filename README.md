# Определения

**Выражение** - это кусочек кода, который вычисляется в какое-то значение. Их можно использовать везде, где ожидается какое-то значение. Примеры выражений:

* константы
```javascript
console.log(50); // 50 -константа(не меняется)
```
* чтение значения переменной
```javascript
const a = 6; 
const b = a; // а - выражение
```
* математические и логические операции
```javascript
console.log(5+6); // 5+6 - выражение
```
* вызов функции, которая возвращает значение
```javascript
function add(x, y){
    const p =x*y;
    const s = x + y;
    return s;
} 

console.log(add(5, 6)); // add(5, 6) - выражение
```

***Блок кода*** - это несколько инструкций, сгрупированных вместе. Если блок кода состоит из нескольких строк, то он должен заключаться в фигурные скобки.

# 1. Переменные
Переменные - это способ дать имя значению.
Из переменной можно прочитать значение, и в переменную можно записать значение.

В JS переменные задаются так:
```javascript
var a; // объявление переменной а. Сейчас так не делают.
let b; // объявление переменной b, которой можно присваивать новое значение.
const c = 10; // объявление переменной с и присваивание ей значения. Больше этой переменной присваивать значений нельзя.
```

В переменную можно записать значение:
```javascript
let a;
a = 10;
a = 20;
```

 Из переменной можно прочитать значение:
 ```javascript
 let a = 10;
 console.log(a); // выводим значение а на консоль( чтоб было видно в консоли).
 let b = a; // переменной можно присвоить значение другой переменной.
 ```

 С переменной можно обращаться так же, как и со значением:
```javascript
let a = 10;
let b = a*5; // b == 50
```

## Правила именования переменных:
* Имя переменной должно начинаться с буквы или знака подчеркивания
```javascript
let _ao_ = 10;
let ero; 
```

* Имя переменной может содержать буквы, цифры, знак подчеркивания
```javascript
let _3f6_;
let a3456;
let __ee_5 = 34;
```

* Переменные обычно называют с маленькой буквы, если название переменной включает несколько слов,то каждение слово начинается с большой буквы(не включая заглавную)
```javascript
let smoke;
let smokingIsBadForOurLife;
```

# 2. Функции

Функция - это кусочек кода, у которого есть имя и ноль или больше параметров. Функция объявляется один раз, и потом может быть вызвана несколько раз, возможно с разными аргументами.

Функция может возвращать значение(а может и нет).

## 2.1 Объявление функции

```javascript
function add(x, y){
    return x + y;
}
```
Объявление функции начинается с ключевого слова `function`, далее через пробел идет имя функции, круглые скобки, внутри скобок список параметров через запятую и тело функции, заключенное в фигурные скобки. Внутри тела функции может использоваться ключевое слово `return`, при помощи которого из функции возвращается значение.

В теле функции можно писать практически любой код: объявлять переменные, вызывать другие функции, писать циклы, условия, даже объявлять другие функции.

Правила для имен функции и параметров функции такие же, как и для переменных. 

Примеры:
```javascript
function printSum(p, o){
    console.log(p+o)
}
```
```javascript
function add(u, i, y){
    return (u+i)*y;
}

```
```javascript
function add(u, i, y){
   const s = u+i;
   console.log(s)
    return s*y;
}

```

## 2.2 Вызов функции

Функция вызывается по имени. После имени обязательно указываются круглые скобки. Если у функции есть аргументы, они перечисляются внутри круглых скобок через запятую в том же порядке, как и параметры функции.

Параметры - в объявлении функции, аргументы - значения параметров при вызове функции.

Примеры:
```javascript
function add(x, y){
    return x + y;
}

const s = add(5, 7)
```
```javascript
function print(x){
    console.log(x);
}

function square(p){
    return p*p;
}

```

## 3. Литералы

Литерал - это значение определенного типа, записанное в коде. 

Примеры:
* литерал числа: 
```javascript
сonst a = 5.4; // дробные числа пишуться всегда с точкой
```
* литерал строки, можно использовать двойные, одинарные или обратные кавычки.
```javascript
const a = "Hello, I am Elya."; 
const b = 'I live in Kharkiv.';
const c = `I am 15 years old.`;
const d = `Info about me: ${a} ${b} ${c}`; // строки подстановки, можно вставлять значения выражения внутрь строки
```

* литерал логического типа: 
```javascript
const yes = true;
const no = false; 
```
* литерал объекта

* литерал массива

* литерал отсутствующего значения `undefined`. Это значение объявленой переменной, которой не присвоено значение:
```javascript
let a; // a === undefined
```

* литерал пустого значения `null`


## 4. Логические выражения 

Логическое выражение - это выражение сравнения двух значений. 
* операторы сравнения

```javascript
console.log(1 > 2); // false
console.log(2*2 >= 1); // true 
console.log("Lama" === ("La" + "ma")); // true
console.log("Hi" !== "OMG"); // true
```

* логические операторы

`&&` - логическое И.

`||` - логическое ИЛИ.

`!` - логическое НЕ.
```javascript
console.log(true && true); // true
console.log(false || true); // true
console.log((2*5 < 10) || (3*6 === 20)); // false
console.log(
    (3*3 === 10) || 
    (("Cafe" === "Sweeter") && (17 - 10 === 7))
); // false
```

## 5. Условный оператор 

Условный оператор позволяет выполнять блок кода, если какое-то условие истинно. Условный оператор имеет вид:
```javascript
if(condition) {
    // condition is true
} else {
    // condition is false
}
```
`condition` - выражение, которое вычисляется в `true` или `false`

блок `else` не обязателен


