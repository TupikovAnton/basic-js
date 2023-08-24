# Базовый Javascript

⚠️ НЕ ОТПРАВЛЯЙТЕ ПУЛЛРЕКВЕСТЫ В ЭТОТ РЕПОЗИТОРИЙ ⚠️

## Общее описание задачи

Ваша задача — написать несколько функций, являющихся решением подзадач. Описания подзадач, а также инструкции по запуску тестов и отправке решений находятся ниже.

---

### **Сосчитай котов!**

Ваша задача — сосчитать котов, спрятавшихся на заднем дворе (представленном в виде двумерного массива, `Array`). Коты прячутся хорошо, но их **ушки** (`"^^"`) видны очень хорошо. Ваша задача — реализовать функцию `countCats(backyard)`, которая сосчитает котов. Удачи!

Число найденных котов должно иметь тип `number`. Если коты не найдены, функция должна вернуть `0`.

Напишите ваш код в `src/count-cats.js`.

---

### **Команда мечты**

Представьте себе, что вы с вашими друзьями решаете создать **команду мечты**. Эта команда должна иметь крутое секретное название, которое содержит зашифрованную информацию о ней (или в котором зашифрована информация о ней). Например, это могут быть **первые буквы** имен ее членов **в верхнем регистре**, **отсортированные по алфавиту**.

Ваша задача — реализовать функцию `createDreamTeam(members)`, которая возвращает имя только что созданной команды (`string`), основанной на именах ее членов (`array`). Удачи!

Имена членов команды должны быть типа `string`. Значения другого типа должны быть проигнорированы. В случае неправильного типа `members`  функция должна вернуть `false`.

NB! Имя члена команды может содержать **пробелы**.

Например:

`createDreamTeam(['Matt', 'Ann', 'Dmitry', 'Max'])` => `'ADMM'`

`createDreamTeam(['Olivia', 1111, 'Lily', 'Oscar', true, null])` => `'LOO'`

Напишите ваш код в `src/dream-team.js`.

---

### **Какая пора года??**

Ваша задача — реализовать функцию `getSeason(date)`, которая принимает объект `Date` и возвращает соответствующую ему пору года. Пора года должна быть типа `string`.

Если аргумент `date` не был передан, функция должна вернуть строку `'Unable to determine the time of year!'` Если аргумент `date` **некорректный**, функция должна выбросить ошибку.

Тссс! Среди аргументов, которые попадают в эту функцию, затесался вражеский агент.

![Disguised](https://www.famousbirthdays.com/faces/disguised-toast-image.jpg)

Он руководствуется знаменитой поговоркой: "Если это выглядит как **утка**, плавает как **утка**, и крякает как **утка**, тогда это, скорее всего, **утка** (и неважно, что это **на самом деле**)". Он **искусно маскируется** под настоящую дату (тип `date`), но умелый javascript-разработчик может поймать его и выбросить ошибку как раз вовремя!

Напишите ваш код в `src/what-season.js`.

---

### **Преобразование массива**

Ваша задача — реализовать функцию `transform(arr)`, которая принимает массив (тип `array`) и возвращает **преобразованный** массив, основываясь на **управляющих последовательностях**, которые содержит. **Управляющие последовательности** — это определенные строковые элементы вышеупомянутого массива:
* `--discard-next` исключает следующий за ней элемент массива из преобразованного массива.
* `--discard-prev` исключает предшествующий ей элемент массива из преобразованного массива.
* `--double-next` удваивает следующий за ней элемент массива в преобразованном массиве.
* `--double-next` удваивает предшествующий ей элемент массива в преобразованном массиве.

Например:

`transform([1, 2, 3, '--double-next', 4, 5])` => `[1, 2, 3, 4, 4, 5]`

`transform([1, 2, 3, '--discard-prev', 4, 5])` => `[1, 2, 4, 5]`

Функция не должна изменять исходный массив. Управляющие последовательности применяются **последовательно, слева направо**. Управляющие последовательности **не попадают** в преобразованный массив. Управляющие последовательности в исходном массиве не встречаются подряд (не следуют одна за другой). Если около управляющей последовательности **нет элемента**, к которому она может быть применена, **она не делает ничего**. Функция должна выбросить ошибку, если `arr` не является массивом. 

Напишите свой код в `src/transform-array.js`.

---

### **Рекурсивный вычислитель глубины**
![Идти глубже](https://i.imgur.com/k7lADiM.jpg)

Ваша задача — реализовать класс `DepthCalculator` с методом `calculateDepth`, который принимает массив и возвращает его **глубину**.

Метод `calculateDepth` должен проходить полученный массив **рекурсивно**. Глубина **плоского** массива — 1. Метод должен корректно работать с массивами, не содержащими элементов или содержащими пустые массивы.

Например:

`const depthCalc = new DepthCalculator();`
`const { calculateDepth } = depthCalc;`

`calculateDepth([1, 2, 3, 4, 5])` => `1`

`calculateDepth([1, 2, 3, [4, 5]])` => `2`

`calculateDepth([[[]]])` => `3`

Напишите ваш код в `src/recursive-depth.js`.

---

#### Предварительные шаги
1. Устаовите [Node.js](https://nodejs.org/en/download/)    
2. Перейдите в папку `basic-js`  
3. Вбейте в командную строку [`npm install`](https://docs.npmjs.com/cli/install) для установки зависимостей  
4. Выполните `npm run test` в командой строке.
5. Вы увидите число ожидающих (pending), проходящих и падающих тестов. 100% проходящие тесты сооветствуют 100 очкам в скор.