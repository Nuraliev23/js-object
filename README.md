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
