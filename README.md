# Тема 3. Операторы, условия, циклы
Отчет по Теме #8 выполнил:
- Чемезов Михаил Владимирович
- АИС-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
- Создайте класс “Car” с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.
### Код
```python
class Car:
    def _init_(self, make, model):
        self.make = make
        self.model = model


my_car = Car("Lada", "Granta")
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L1_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L1_2.png)
### Вывод:
- Код создает класс "Car" с двумя атрибутами: "make" (марка) и "model" (модель) автомобиля.
- Конструктор класса "init" принимает два параметра "make" и "model"
- Инициализируются соответствующие атрибуты объекта класса Car.
- Далее, создается экземпляр класса "my_car" с аргументами "Lada" (марка) и "Granta" (модель)
- Таким образом, переменная "my_car" будет ссылаться на объект класса "Car" с атрибутами make="Lada" и model="Granta".

## Лабораторная работа №2
- Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину “поехать”. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
### Код
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model


    def drive(self):
        print(f"Driving the {self.make} {self.model}")


my_car = Car("Lada", "Granta")
my_car.drive()
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L2_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L2_2.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L2_3.png)
### Вывод:
- Создается объект "my_car" класса "Car" с аргументами "Lada" и "Granta".
- Форматируется строка, чтобы значения атрибутов "self.make" и "self.model" подставились в нужные места.
- Код выводит на экран строку, состоящую из значения атрибута "self.make", значения атрибута "self.model" и текста "Driving the";
- Вызывается метод "drive()" у этого объекта, в результате чего выводится на экран "Driving the Lada Granta".

## Лабораторная работа №3
- Создайте новый класс “ElectricCar” с методом “charge” и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться.
Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
### Код
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model


    def drive(self):
        print(f"Driving the {self.make} {self.model}")


my_car = Car("Lada", "Granta")
my_car.drive()

class ElectricCar(Car):
    def __init__(self, make, model, battery_capacity):
        super().__init__(make, model)
        self.battery_capacity = battery_capacity


    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")


my_electric_car = ElectricCar("Nissan", "Ariya", 78)
my_electric_car.drive()
my_electric_car.charge()
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L3_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L3_2.png)
### Выводы:
- Класс Car имеет конструктор __init__, который принимает make и model в качестве параметров и инициализирует соответствующие переменные экземпляра.
- Класс Car имеет метод drive, который выводит сообщение о том, что машина в движении.
- подкласс ElectricCar класса Car имеет свой собственный __init__, который расширяет __init__ класса Car с помощью super().
- подкласс ElectricCar принимает дополнительный параметр battery_capacity и инициализирует новую переменную экземпляра.
- подкласс ElectricCar имеет метод charge, который выводит сообщение о том, что электромобиль заряжается.
- Создаются экземпляры классов (my_car и my_electric_car), и вызываются их методы drive и charge.
- Выводятся сообщения: driving the Lada Granta, driving the Nissan Ariya и charging the Nissan Ariya with 78 kWh
  
## Лабораторная работа №4
- Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
### Код
```python
class Car:
    def __init__(self, make, model):
        self._make = make
        self.__model = model


    def drive(self):
        print(f"Driving the {self._make} {self.__model}")


my_car = Car("Lada", "Granta")
print(my_car._make)
#print(my_car.__model)
my_car.drive()
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L4_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L4_2.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L4_3.png)
### Выводы:
- Класс Car имеет два атрибута: _make и __model.
- Атрибут _make считается защищенным (по соглашению) и может быть доступен напрямую.
- Атрибут __model считается приватным, что усложняет прямой доступ извне класса. Попытка доступа к нему напрямую вызовет AttributeError.
- Метод drive выводит сообщение о том, что машина находится в движении, используя значения атрибутов _make и __model.
- print(my_car._make) выводит Lada
- print(my_car._make) выводит AttributeError

## Лабораторная работа №5
- Реализуйте полиморфизм создав основной (общий) класс “Shape”, а также еще два класса “Rectangle” и “Circle”. Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
### Код
```python
class Shape:
    def area(self):
        pass


class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height


    def area(self):
        return self.width * self.height


class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius


# Создание объектов
rectangle = Rectangle(5, 4)
circle = Circle(3)

# Создание массива с фигурами
shapes = [rectangle, circle]

# Вывод площадей фигур
for shape in shapes:
    print(shape.area())
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/L5.png)
### Выводы:
- Определение базового класса 'Shape' с методом 'area'. Метод 'area' будет переопределен в подклассах.
- Определение подкласса 'Rectangle', наследующего от 'Shape' где реализуется метод-конструктор для инициализации ширины и высоты. Переопределение метода 'area' для вычисления площади прямоугольника.
- Определение еще одного подкласса 'Circle', также наследующего от 'Shape' где реализуется метод-конструктор для инициализации радиуса. Переопределение метода 'area' для вычисления площади круга.
- Создание объектов классов 'Rectangle' и 'Circle' и массива 'shapes', содержащего объекты 'rectangle' и 'circle'
- Перебор элементов массива 'shapes' и вывод площади каждой фигуры

## Самостоятельная работа №1
- Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
### Код
```python
class Fruit:
    def __init__(self, name, color, taste):
        self.name = name
        self.color = color
        self.taste = taste


# Создаем объекты
apple = Fruit("Яблоко", "красный", "сладкий")
banana = Fruit("Банан", "желтый", "сладкий и ароматный")
orange = Fruit("Апельсин", "оранжевый", "кисло-сладкий")

# Выводим некоторые свойства объектов
print(apple.color)
print(orange.taste)
print(banana.name)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I1.png)
### Выводы:
- 'num = 1' создается переменная с именем num и присваивается ей значение 1.
- Затем выполняется цикл for два раза (for _ in range(2):). Прочерк (_) часто используется в Python, когда итерационная переменная цикла for не используется внутри самого цикла.
- Внутри цикла, в строке num *= 5, значение num умножается на 5, а затем новое значение присваивается num (num = num * 5).
- Затем, на следующей строке num += 1, выполнится операция инкремента: к num добавляется 1 (num = num + 1).
- После завершения цикла, последней строкой (print(num)) выводится результат - текущее значение переменной num.
- Выполнение кода:
-- num = 1
-- Первая итерация цикла (num * 5 + 1 = 6)
-- Вторая итерация цикла (num * 5 + 1 = 31)
-- Будет число 31.

## Самостоятельная работа №2
- Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
### Код
```python
class Fruit:
    def __init__(self, name, color, taste):
        self.name = name
        self.color = color
        self.taste = taste

    def properties(self):
        return f"{self.name} имеет {self.color} цвет и вкус {self.taste}"


# Создаем объекты
apple = Fruit("Яблоко", "красный", "сладкий")
banana = Fruit("Банан", "желтый", "сладкий и ароматный")
orange = Fruit("Апельсин", "оранжевый", "кисло-сладкий")

# Используем методы объектов
print(apple.properties())
print(banana.properties())
print(orange.properties())
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I2.png)
### Выводы:
- 'message = "Hello World"' Здесь объявляется переменная message, которая содержит строку "Hello World".
- 'for i in range(len(message)-1, -1, -1):' : Здесь устанавливается цикл for. Указанная функция range() создает последовательность чисел от len(message)-1 до 0. len(message)-1 является индексом последнего символа в строке (поскольку индексы в Python начинаются с 0), и -1 является индексом, следующим за первым, что позволяет включить в последовательность и 0. Шаг -1 указывает, что каждая следующая итерация должна происходить в обратном порядке.
- 'print(message[i])' : Здесь каждый символ строки message выводится по одному, начиная с конца и идя к началу.
- Исходное сообщение выводится в обратном порядке одним символом на каждой строке.
  
## Самостоятельная работа №3
- Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
### Код
```python
class Fruit:
    def __init__(self, name, color, taste):
        self.name = name
        self.color = color
        self.taste = taste

    def properties(self):
        return f"{self.name} имеет {self.color} цвет и вкус {self.taste}"


# Создаем объекты
apple = Fruit("Яблоко", "красный", "сладкий")
banana = Fruit("Банан", "желтый", "сладкий и ароматный")
orange = Fruit("Апельсин", "оранжевый", "кисло-сладкий")

class ExoticFruit(Fruit):
    def __init__(self, name, color, taste, origin):
        super().__init__(name, color, taste)
        self.origin = origin

    def properties(self):
        return f"{self.name} имеет {self.color} цвет и вкус {self.taste}. Популярное место для выращивания {self.origin}"

pineapple = ExoticFruit("Ананас", "желтый", "сладкий и кислый", "Гавайи")
print(pineapple.properties())
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_2.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_3.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I3_4.png)
### Выводы:
- Запрашивается ввод числа от пользователя в диапазоне от 0 до 10.
- Если введенное значение меньше 0 или больше 10, выводится сообщение "Введенное значение не находится в диапазоне от 0 до 10", а затем программа завершается.
- Иначе, если значение меньше или равно 3, выводится сообщение "Число находится в диапазоне от 0 до 3".
- Иначе, если значение меньше 10, выводится сообщение "Число находится в диапазоне от 3 до 10".
- Иначе (если значение равно 10), выводится сообщение "Число находится в диапазоне от 10".
  
## Самостоятельная работа №4
- Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
### Код
```python
class Fruit:
    def __init__(self, name, color, taste):
        self._name = name
        self._color = color
        self.__taste = taste

    def properties(self):
        return f"{self._name} имеет {self._color} цвет и вкус {self.__taste}"


# Создаем объекты
apple = Fruit("Яблоко", "красный", "сладкий")

# Вызов атрибутов объекта
print(apple._name)
#print(apple.__tasty) #Выводится ошибка
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I4_1.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I4_2.png)
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I4_3.png)
### Выводы:
- Код определяет длину предложения, используя встроенную функцию len(). Эта количество символов в предложении.
- Приводит все символы предложения к нижнему регистру с помощью метода .lower().
- Подсчитывает количество гласных букв в предложении. Цикл for проходит по каждому символу в предложении и, если этот символ присутствует в списке гласных (vowels), увеличивает счетчик вхождения гласных (vowel_count).
- Заменяет все вхождения слова "ugly" на слово "beauty" в предложении с помощью метода .replace().
- Проверяет, начинается ли предложение со слова "The" и заканчивается ли оно словом "end". Для этого используются методы строки .startswith() и .endswith().
  
## Самостоятельная работа №5
- Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
### Код
```python
class Fruit:
    def __init__(self, name, quantity):
        self.name = name
        self.quantity = quantity

    def total(self):
        pass


class Apple(Fruit):
    def __init__(self, quantity):
        super().__init__('Apple', quantity)

    def total(self):
        return self.quantity * 242  # Предположим, что каждое яблоко весит 242 грамма


class Banana(Fruit):
    def __init__(self, quantity):
        super().__init__('Banana', quantity)

    def total(self):
        return self.quantity * 150  # Предположим, что каждый банан весит 150 единицы


# Создание объектов
apple = Apple(5)
banana = Banana(7)

# Создание массива с фруктами
fruits = [apple, banana]

# Вывод общего веса фруктов
for fruit in fruits:
    print(f'Общий вес {fruit.name} в корзине: {fruit.total()}')
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_3/pic/I5.png)
### Выводы:
- Создание строковых переменных memory и string со значениями ' world' и 'hello' соответственно.
-  Создание числовой переменной counter со значением 0 и список values, который содержит значения от 0 до 10 с шагом 2.
- Затем начинается цикл while, который будет выполняться до тех пор, пока counter не станет равным 10.
- Внутри цикла проверка, является ли текущее значение переменной counter одним из значений в списке values. Если значение counter присутствует в values, то на экран выводятся две строки: соединение строк string и memory, а затем просто string. Если значение counter отсутствует в списке values, цикл просто продолжается без действий.
- После проверки значение counter увеличивается на 1 каждый проход цикла.
- Когда цикл завершается (это случится когда counter станет равным 10), происходит соединение строк string и memory, результат которого записывается обратно в string.
- Значение string присваивается переменной memory.
- В конце вы выводите содержимое переменной memory, которая в этот момент будет содержать 'hello world'.

## Общие выводы по теме
- Операторы, условия и циклы в Python являются мощными инструментами, которые позволяют создавать гибкие и эффективные алгоритмы. 
