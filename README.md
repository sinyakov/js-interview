# Вопросы для интервью

## Javascript

1 .В каком порядке выведутся сообщения в консоль?

```js
const intervalId = setInterval(() => {
  console.log('James');
}, 10);

setTimeout(() => {
  const promise = new Promise((resolve) => {
    console.log('Richard');
    resolve('Robert');
  });

  promise
      .then((value) => {
        console.log(value);

        setTimeout(() => {
          console.log('Michael');

          clearInterval(intervalId);
        }, 10);
      });

  console.log('John');
}, 10);
```

2. Вопрос про this

```js
function Person(age) {
    this.age = age;

    setInterval(function() {
        this.age++;
    }, 1000);
}

const vasya = new Person(13);
```

3. Вопрос про прототипы
```js
function Person(name) {
    this.name = name;
}

const juan = new Person('Juan');

Person.prototype = {
    getName: function () {
        return this.name;
    }
};

const pedro = new Person('Pedro');

console.log(pedro.getName());
console.log(juan.getName());
```

4. Map, Set, WeakMap, WeakSet

5. Bind, call, apply — зачем нужны. Реализовать байнд, реализовать кол

6. Посчитать сумму
```js
sum(1)(2)(3) === 6
4..add(3) === 7
add(3)(4) === 7
```

7. Замыкания
```js
const button = document.getElementById('button');

for (var i = 0; i < 3; i++) {
    button.addEventListener('click', function (e) {
        console.log(i);
    });
}

button.trigger(‘click’);
```

## React

1. setState
2. keys
3. Жизненный цикл реакт-компонентов
4. Аналоги shouldComponentUpdate
5. Различие между функциональными и классовыми компонентами
6. Что возвращает метод render
7. Чем отличаются hoc и hook
8. Fiber и история реакта

## Броузер

1. Какими способами мы можем добавить картинку
2. Выставить три дива по горизонтали
3. Адаптирование графики
4. Ссылка внутри ссылки
5. rel: noopener/noreferrer
6. Специфичность селекторов
7. Чем поведение скрипта с атрибутом defer отличается от async?
8. Расскажите всё, что вы знаете о событиях в JS.
9. Что происходит при вводе адреса сайта

## Программирование

- Напишите функцию, принимающую на вход время (в любом формате) и возвращающую угол между стрелками аналоговых часов.
- Написать генератор чисел от а до б
- Заполнить матрицу 10×10 случайными числам от 1 до 100 без повторений
- FizzBuzz
- RLE
- Уникальные значения в массиве
- flat
- sort odd numbers in array
- random hex colour
- Напишите функцию, принимающую на вход строку и проверяющую, является ли эта строка палиндромом. Приведите несколько вариантов решения.
- Напишите функцию, принимающую массив произвольных слов и на выходе дающую двумерный массив анаграмм:
```
['стол', 'барокко', слот', 'кот', 'кошка', 'ток', 'коробка'] →
[['стол', 'слот'], ['кот', 'ток'], ['барокко', 'коробка']]
```
- массив из десяти функций: `arr[3]() // 3`

## Не программирование

- HTTP-протокол
- Cookie
- Принципы ООП
- ФП vs процедурное
- SOLID
- Event loop
- MVP
- REST

