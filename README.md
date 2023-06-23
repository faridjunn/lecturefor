# Массивы JavaScript
Массив — это специальная переменная, которая может содержать более одного значения:
- const cars = ["Saab", "Volvo", "BMW"];

###### Зачем использовать массивы?
Если у вас есть список элементов (например, список названий автомобилей), хранение автомобилей в отдельных переменных может выглядеть так:
###### Зачем использовать массивы?
Если у вас есть список элементов (например, список названий автомобилей), хранение автомобилей в отдельных переменных может выглядеть так:
- let car1 = "Saab";
let car2 = "Volvo";
let car3 = "BMW";

Однако что, если вы хотите перебрать все машины и найти конкретную? А если бы у вас было не 3 машины, а 300?

Решение представляет собой массив!

Массив может содержать множество значений под одним именем, и вы можете получить доступ к значениям, обратившись к порядковому номеру.
###### Создание массива
Использование литерала массива — это самый простой способ создать массив JavaScript.

Синтаксис:
- const array_name = [item1, item2, ...];  

Общепринятой практикой является объявление массивов с помощью ключевого слова const .

### Использование ключевого слова JavaScript new
В следующем примере также создается массив и присваиваются ему значения:
- const cars = new Array("Saab", "Volvo", "BMW");

### Доступ к элементам массива
Вы получаете доступ к элементу массива, обращаясь к номеру индекса :
- const cars = ["Saab", "Volvo", "BMW"];
let car = cars[0];

Примечание. Индексы массива начинаются с 0.

[0] — первый элемент. [1] — второй элемент.

### Изменение элемента массива
Этот оператор изменяет значение первого элемента в cars:
- const cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel"; //Opel,Volvo,BMW

 Array Methods
=
1. pop() ===> Метод pop()удаляет (извлекает) последний элемент массива.
Метод pop()изменяет исходный массив.
Метод pop()возвращает удаленный элемент.
- const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];
console.log(plants.pop());
// Expected output: "tomato"
console.log(plants);
// Expected output: Array ["broccoli", "cauliflower", "cabbage", "kale"]
plants.pop();
console.log(plants);
// Expected output: Array ["broccoli", "cauliflower", "cabbage"]

2. shift() ===> Метод shift()удаляет первый элемент массива.
Метод shift()изменяет исходный массив.
Метод shift()возвращает сдвинутый элемент.
- const array1 = [1, 2, 3];
const firstElement = array1.shift();
console.log(array1);
// Expected output: Array [2, 3]
console.log(firstElement);
// Expected output: 1


3. push() ===> Метод push()добавляет новые элементы в конец массива.
Метод push()изменяет длину массива.
Метод push()возвращает новую длину.
- const animals = ['pigs', 'goats', 'sheep'];
const count = animals.push('cows');
console.log(count);
// Expected output: 4
console.log(animals);
// Expected output: Array ["pigs", "goats", "sheep", "cows"]
animals.push('chickens', 'cats', 'dogs');
console.log(animals);
// Expected output: Array ["pigs", "goats", "sheep", "cows", "chickens", "cats", "dogs"]


4. unshift()  ===> Метод unshift()добавляет новые элементы в начало массива.
Метод unshift()перезаписывает исходный массив.
- const array1 = [1, 2, 3];
console.log(array1.unshift(4, 5));
// Expected output: 5
console.log(array1);
// Expected output: Array [4, 5, 1, 2, 3

5. concat()  ===> Метод concat()объединяет (объединяет) два или более массива.
Метод concat()возвращает новый массив, содержащий объединенные массивы.
Метод concat()не изменяет существующие массивы.
- const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];
const array3 = array1.concat(array2);
console.log(array3);
// Expected output: Array ["a", "b", "c", "d", "e", "f"]

6. slice() ===> Метод splice()добавляет и/или удаляет элементы массива.
Метод splice()перезаписывает исходный массив.
- const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

- console.log(animals.slice(2));
// Expected output: Array ["camel", "duck", "elephant"]

- console.log(animals.slice(2, 4));
// Expected output: Array ["camel", "duck"]

- console.log(animals.slice(1, 5));
// Expected output: Array ["bison", "camel", "duck", "elephant"]

7. join()  ===> Метод join()возвращает массив в виде строки.
Метод join()не изменяет исходный массив.
Можно указать любой разделитель. По умолчанию используется запятая (,).
- const elements = ['Fire', 'Air', 'Water'];
console.log(elements.join());
// Expected output: "Fire,Air,Water"

- console.log(elements.join(''));
// Expected output: "FireAirWater"

- console.log(elements.join('-'));
// Expected output: "Fire-Air-Water"

8. includes() ===> Метод includes()возвращает значение true , если массив содержит указанное значение.
Метод includes()возвращает значение false, если значение не найдено.
Метод includes()чувствителен к регистру.
- const array1 = [1, 2, 3];
console.log(array1.includes(2));
// Expected output: true
- const pets = ['cat', 'dog', 'bat'];
console.log(pets.includes('at'));
// Expected output: false

9. indexOf() ===> Метод indexOf()возвращает первый индекс (позицию) указанного значения.
Метод indexOf()возвращает -1, если значение не найдено.
Метод indexOf()начинается с указанного индекса и выполняет поиск слева направо.
По умолчанию поиск начинается с первого элемента и заканчивается последним.
Отрицательные начальные значения отсчитываются от последнего элемента (но поиск по-прежнему осуществляется слева направо).
- const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];
console.log(beasts.indexOf('bison'));
// Expected output: 1

- // Start from index 2
console.log(beasts.indexOf('bison', 2));
// Expected output: 4

- console.log(beasts.indexOf('giraffe'));
// Expected output: -1

10. splice()  ===> Метод splice()добавляет и/или удаляет элементы массива.
Метод splice()перезаписывает исходный массив.
- const months = ['Jan', 'March', 'April', 'June'];
months.splice(1, 0, 'Feb');
// Inserts at index 1
console.log(months);
// Expected output: Array ["Jan", "Feb", "March", "April", "June"]

- months.splice(4, 1, 'May');
// Replaces 1 element at index 4
console.log(months);
// Expected output: Array ["Jan", "Feb", "March", "April", "May"]

11. toString()  ===> Метод toString()возвращает строку со значениями массива, разделенными запятыми.
Метод toString()не изменяет исходный массив.
- const array1 = [1, 2, 'a', '1a'];
console.log(array1.toString());
// Expected output: "1,2,a,1a"

12. toReversed()  ===> Метод toReversed()экземпляров Arrayявляется копирующим аналогом метода reverse(). Он возвращает новый массив с элементами в обратном порядке.
  - const reversedItems = items.toReversed();
console.log(reversedItems); // [3, 2, 1]
console.log(items); // [1, 2, 3]

13. forEach() ===> Метод forEach()вызывает функцию для каждого элемента массива.
Метод forEach()не выполняется для пустых элементов.
- forEach(callbackFn)
forEach(callbackFn, thisArg)
- const array1 = ['a', 'b', 'c'];
array1.forEach(element => console.log(element));
// Expected output: "a"
// Expected output: "b"
// Expected output: "c"

14. map()  ===> map()создает новый массив из вызова функции для каждого элемента массива.
map()не выполняет функцию для пустых элементов.
map()не изменяет исходный массив.
- const array1 = [1, 4, 9, 16];
// Pass a function to map
const map1 = array1.map(x => x * 2);
console.log(map1);
// Expected output: Array [2, 8, 18, 32]

15. find() ===> Метод find()возвращает значение первого элемента, прошедшего проверку.
Метод find()выполняет функцию для каждого элемента массива.
Метод find()возвращает значение undefined, если элементы не найдены.
Метод find()не выполняет функцию для пустых элементов.
Метод find()не изменяет исходный массив.
- const array1 = [5, 12, 8, 130, 44];
const found = array1.find(element => element > 10);
console.log(found);
// Expected output: 12

16. filter() ===> Метод filter()создает новый массив, заполненный элементами, прошедшими проверку, предоставляемую функцией.
Метод filter()не выполняет функцию для пустых элементов.
Метод filter()не изменяет исходный массив.
- filter(callbackFn)
filter(callbackFn, thisArg)
- const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
const result = words.filter(word => word.length > 6);
console.log(result);
// Expected output: Array ["exuberant", "destruction", "present"]

17. reduce()  ===> Метод reduce()выполняет функцию редуктора для элемента массива.
Метод reduce()возвращает одно значение: накопленный результат функции.
Метод reduce()не выполняет функцию для пустых элементов массива.
Метод reduce()не изменяет исходный массив.
- reduce(callbackFn)
reduce(callbackFn, initialValue)
- const array1 = [1, 2, 3, 4];
// 0 + 1 + 2 + 3 + 4
const initialValue = 0;
const sumWithInitial = array1.reduce(
  (accumulator, currentValue) => accumulator + currentValue,
  initialValue
);
console.log(sumWithInitial);
// Expected output: 10

18. toSorted()  ===> Метод toSorted()экземпляров Arrayявляется копирующей версией метода sort(). Он возвращает новый массив с элементами, отсортированными в порядке возрастания.
- const values = [1, 10, 21, 2];
const sortedValues = values.toSorted((a, b) => a - b);
console.log(sortedValues); // [1, 2, 10, 21]
console.log(values); // [1, 10, 21, 2]

19. sort()  ===> Сортирует sort()элементы массива.
перезаписывает sort()исходный массив.
Сортирует sort()элементы как строки в алфавитном и возрастающем порядке.
- sort()
sort(compareFn)
- const array1 = [1, 30, 4, 21, 100000];
array1.sort();
console.log(array1);
// Expected output: Array [1, 100000, 21, 30, 4]


20. reverse()  ===> Метод reverse()меняет порядок элементов в массиве на обратный.
Метод reverse()перезаписывает исходный массив.
- const numbers = [3, 2, 4, 1, 5];
const reversed = numbers.reverse();
// numbers and reversed are both in reversed order [5, 1, 4, 2, 3]
reversed[0] = 5;
console.log(numbers[0]); // 5

JavaScript array methods callbacks
=
1. map()
2. forEach()
3. find()
4. reduce() 
5. filter()
6. toSorted()

#### 1. Остаточные параметры (rest parameters)  
 Синтаксис остаточных параметров функции позволяет представлять неограниченное множество аргументов в виде массива.
- function sum(...theArgs) {
  let total = 0;
  for (const arg of theArgs) {
    total += arg;
  }
  return total;
}
console.log(sum(1, 2, 3));
// Expected output: 6
- console.log(sum(1, 2, 3, 4));
// Expected output: 10

Если последний именованный аргумент функции имеет префикс ..., он автоматически становится массивом с элементами от 0 до theArgs.length-1 в соответствии с актуальным количеством аргументов, переданных в функцию.
- function myFun(a, b, ...manyMoreArgs) {
  console.log("a", a);
  console.log("b", b);
  console.log("manyMoreArgs", manyMoreArgs);
}
myFun("один", "два", "три", "четыре", "пять", "шесть");
// Console Output:
// a, один
// b, два
// manyMoreArgs, [три, четыре, пять, шесть]

Поскольку theArgs является массивом, количество элементов в нём определяется свойством length:
- function fun1(...theArgs) {
  console.log(theArgs.length);
}
fun1();  // 0
fun1(5); // 1
fun1(5, 6, 7); // 3

#### 2. Синтаксис распространения (...)   (Spread)
###### Оператор спреда
Оператор расширения JavaScript ( ...) расширяет итерируемый объект (например, массив) на большее количество элементов.

Это позволяет нам быстро копировать весь существующий массив или его части в другой массив:
Пример
Присвойте первый и второй элементы from numbersпеременным, а остальные поместите в массив:
- const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];  //1,2,3,4,5,6

Оператор распространения часто используется для извлечения из массива только того, что необходимо:
- const numbers = [1, 2, 3, 4, 5, 6];
const [one, two, ...rest] = numbers; 

Мы также можем использовать оператор распространения с объектами:
- const myVehicle = {
  brand: 'Ford',
  model: 'Mustang',
  color: 'red'
}
const updateMyVehicle = {
  type: 'car',
  year: 2021,
  color: 'yellow'
}
const myUpdatedVehicle = {...myVehicle, ...updateMyVehicle}

#### 3. Назначение деструктурирования
Синтаксис деструктурирующего присваивания — это выражение JavaScript, позволяющее распаковывать значения из массивов или свойства объектов в отдельные переменные.
- let a, b, rest;
[a, b] = [10, 20];
console.log(a);
// Expected output: 10
console.log(b);
// Expected output: 20
[a, b, ...rest] = [10, 20, 30, 40, 50];
console.log(rest);
// Expected output: Array [30, 40, 50]

Литеральные выражения объекта и массива обеспечивают простой способ создания специальных пакетов данных.
- const x = [1, 2, 3, 4, 5];

 Назначение деструктурирования использует аналогичный синтаксис, но в левой части назначения, чтобы определить, какие значения распаковывать из исходной переменной.
- const x = [1, 2, 3, 4, 5];
const [y, z] = x;
console.log(y); // 1
console.log(z); // 2

 Точно так же вы можете деструктурировать объекты в левой части задания.
 - const obj = { a: 1, b: 2 };
const { a, b } = obj;
// is equivalent to:
// const a = obj.a;
// const b = obj.b;

Эта возможность аналогична функциям, присутствующим в таких языках, как Perl и Python.


