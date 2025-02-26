# Object
Тип Object представляет один из типов данных JavaScript. Он используется для хранения различных коллекций с ключами и более сложных сущностей. Объекты могут быть созданы с использованием конструктора Object() или синтаксиса инициализатора / литерала объекта.
### Описание
Почти все объекты в JavaScript являются экземплярами Object; типичный объект наследует свойства (включая методы) от Object.prototype, хотя эти свойства могут быть затенены (т.е. переопределены). Единственные объекты, которые не наследуют от Object.prototype, - это те, у которых прототип null, или которые происходят от других объектов с прототипом null.

Изменения в объекте Object.prototype видны всем объектам с помощью цепочки прототипов, если свойства и методы, подверженные этим изменениям, не переопределены дальше по цепочке прототипов. Это предоставляет очень мощный, хотя и потенциально опасный механизм для переопределения или расширения поведения объектов. Для обеспечения большей безопасности, Object.prototype - единственный объект в основном языке JavaScript, у которого неизменяемый прототип - прототип Object.prototype всегда null и не может быть изменен.

### Синтаксис
// Инициализатор объекта или литерал
{ [ nameValuePair1[, nameValuePair2[, ...nameValuePairN] ] ] }

// Вызов в качестве конструктора
new Object([value])
### Параметры
nameValuePair1, nameValuePair2, ... nameValuePairN
Пары из имён (строки) и значений (любые значения), где имя отделяется от значения двоеточием.

value
Любое значение.

# Свойства конструктора Object
Object.length
Имеет значение 1.

Object.prototype
Позволяет добавлять свойства ко всем объектам типа Object.
Методы конструктора Object
Object.assign()
Создаёт новый объект путём копирования значений всех собственных перечислимых свойств из одного или более исходных объектов в целевой объект.

Object.create()
Создаёт новый объект с указанными объектом прототипа и свойствами.

Object.defineProperty()
Добавляет к объекту именованное свойство, описываемое переданным дескриптором.

Object.defineProperties()
Добавляет к объекту именованные свойства, описываемые переданными дескрипторами.

Object.freeze()
Замораживает объект: другой код не сможет удалить или изменить никакое свойство.

Object.getOwnPropertyDescriptor()
Возвращает дескриптор свойства для именованного свойства объекта.

Object.getOwnPropertyNames()
Возвращает массив, содержащий имена всех переданных объекту собственных перечисляемых и неперечисляемых свойств.

Object.getOwnPropertySymbols()
Возвращает массив всех символьных свойств, найденных непосредственно в переданном объекте.

Object.getPrototypeOf()
Возвращает прототип указанного объекта.

Object.is()
Определяет, являются ли два значения различимыми (то есть, одинаковыми)

Object.isExtensible()
Определяет, разрешено ли расширение объекта.

Object.isFrozen()
Определяет, был ли объект заморожен.

Object.isSealed()
Определяет, является ли объект запечатанным (sealed).

Object.keys()
Возвращает массив, содержащий имена всех собственных перечислимых свойств переданного объекта.

Object.observe()
Асинхронно наблюдает за изменениями в объекте.

Object.preventExtensions()
Предотвращает любое расширение объекта.

Object.seal()
Предотвращает удаление свойств объекта другим кодом.

Object.setPrototypeOf()
Устанавливает прототип (т.е. внутреннее свойство [[Prototype]])
# Экземпляры и прототип объекта Object
Экземпляры и прототип объекта Object

Object.keys() is a built-in JavaScript method that returns an array of a given object's own enumerable property names (keys). It only returns the keys of the object itself, not the ones it inherits from its prototype chain.

Syntax:
javascript
Копировать
Object.keys(obj)
Parameters:
obj: The object whose own enumerable property names you want to retrieve.
Return Value:
An array of strings representing the keys of the object's own properties.
Example:
javascript
Копировать
const person = {
  name: 'Alice',
  age: 30,
  city: 'New York'
};

const keys = Object.keys(person);
console.log(keys); // Output: ["name", "age", "city"]
In this example, Object.keys(person) returns an array of keys: ["name", "age", "city"].

Key Points:
Only the object's own properties are returned (not properties inherited through the prototype chain).
The order of the keys in the array is the same as the order in which they were defined (for non-integer keys).

Object.values() is a built-in JavaScript method that returns an array of the values of a given object's own enumerable properties. It doesn't include properties from the object's prototype chain.

Syntax:
javascript
Копировать
Object.values(obj)
Parameters:
obj: The object whose own enumerable property values you want to retrieve.
Return Value:
An array containing the values of the object's own properties.
Example:
javascript
Копировать
const person = {
  name: 'Alice',
  age: 30,
  city: 'New York'
};

const values = Object.values(person);
console.log(values); // Output: ["Alice", 30, "New York"]
In this example, Object.values(person) returns an array of the values: ["Alice", 30, "New York"].

Key Points:
Similar to Object.keys(), but instead of returning the keys, it returns the values associated with those keys.
The order of the values in the array is the same as the order of the keys in the object (for non-integer keys).
It only returns the values of the object's own properties, not inherited properties.



Object.entries() is a built-in JavaScript method that returns an array of a given object's own enumerable property [key, value] pairs. Each element of the array is itself an array with two elements: the first being the key and the second being the value.

Syntax:
javascript
Копировать
Object.entries(obj)
Parameters:
obj: The object whose own enumerable property [key, value] pairs you want to retrieve.
Return Value:
An array of arrays, where each inner array contains two elements: the key and the value of each property.
Example:
javascript
Копировать
const person = {
  name: 'Alice',
  age: 30,
  city: 'New York'
};

const entries = Object.entries(person);
console.log(entries); 
// Output: [["name", "Alice"], ["age", 30], ["city", "New York"]]
In this example, Object.entries(person) returns an array of key-value pairs:

css
Копировать
[["name", "Alice"], ["age", 30], ["city", "New York"]]
Key Points:
Object.entries() gives you both the keys and the corresponding values of the object's own properties.
The order of the key-value pairs in the array is the same as the order in which the properties were defined (for non-integer keys).
It doesn't include properties from the object's prototype chain, only the object's own enumerable properties.
Common Use Case:
You can use Object.entries() in loops like for...of to iterate over both keys and values:

javascript
Копировать
for (const [key, value] of Object.entries(person)) {
  console.log(`${key}: ${value}`);
}
// Output:
// name: Alice
// age: 30
// city: New York

In JavaScript, the this keyword refers to the context in which a function is called. It is a special variable that provides a reference to the object in which the current code is executing. The value of this depends on how a function is called, and it behaves differently in different contexts.

Key Points:
this is determined at runtime, not at the time of function definition.
The value of this can refer to different objects, depending on the execution context.
It is often used inside methods to refer to the object the method is a part of.
Common Cases for this:
In a Method: When a function is used as a method of an object, this refers to the object the method is called on.

javascript
Копировать
const person = {
  name: 'Alice',
  greet: function() {
    console.log(`Hello, my name is ${this.name}`);
  }
};

person.greet(); // Output: Hello, my name is Alice
Here, this.name refers to the name property of the person object.

In a Function (Global context): In non-strict mode, if you use this inside a regular function, it refers to the global object (window in browsers or global in Node.js).

javascript
Копировать
function show() {
  console.log(this); // In a browser, this refers to the window object
}

show();
In strict mode ('use strict';), this will be undefined in a regular function:

javascript
Копировать
'use strict';
function show() {
  console.log(this); // Output: undefined
}

show();
In an Arrow Function: Arrow functions do not have their own this value. Instead, they inherit this from the surrounding lexical context (the place where the function was created).

javascript
Копировать
const person = {
  name: 'Alice',
  greet: () => {
    console.log(this.name); // 'this' is inherited from the outer context, not the person object
  }
};

person.greet(); // Output: undefined (if in the global context)
In this example, the arrow function does not get this from the person object, but rather from the outer (global) context.

In a Constructor Function: In a constructor function (i.e., when you use new), this refers to the newly created instance of the object.

javascript
Копировать
function Person(name) {
  this.name = name;
}

const alice = new Person('Alice');
console.log(alice.name); // Output: Alice
Here, this refers to the newly created alice object.

Event Handlers: In event handlers, this refers to the element that fired the event.

javascript
Копировать
const button = document.querySelector('button');
button.addEventListener('click', function() {
  console.log(this); // Output: the button element that was clicked
});
Explicit Binding (call, apply, and bind): You can explicitly set the value of this using call(), apply(), or bind().

javascript
Копировать
function greet() {
  console.log(`Hello, ${this.name}`);
}

const person = { name: 'Alice' };

greet.call(person); // Output: Hello, Alice
greet.apply(person); // Output: Hello, Alice

const boundGreet = greet.bind(person);
boundGreet(); // Output: Hello, Alice
Summary:
this refers to the context in which the function is executed.
In methods, this refers to the object the method is a part of.
In a regular function (non-strict mode), this refers to the global object.
In arrow functions, this is inherited from the surrounding context.
In constructors and event handlers, this has specific behaviors that depend on how the function is called.


