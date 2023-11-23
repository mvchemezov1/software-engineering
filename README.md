# Тема 8. Введение в ООП
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
- В этом коде создается класс Fruit, который имеет три атрибута: name, color и taste.
- Затем создаются три объекта класса Fruit - apple, banana и orange - с разными значениями атрибутов.
- Выводятся некоторые свойства этих объектов с помощью команды print.

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
- Создание класса Fruit, который имеет атрибуты name, color и taste, и метод properties(), который выводит информацию о фрукте на основе его атрибутов.
- Создание трёх объектов (apple, banana и orange) класса Fruit с различными свойствами (имя, цвет и вкус). Метод properties() вызывается для каждого объекта, чтобы вывести информацию о каждом фрукте.
  
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
- Создание класса Fruit который определяет основные характеристики фруктов, такие как имя, цвет и вкус.
- Создание класса ExoticFruit. Класс ExoticFruit является подклассом Fruit и добавляет новое свойство - популярное место для выращивания фрукта. Метод properties() в каждом классе выводит информацию о фрукте, его цвете, вкусе и в случае экзотических фруктов - о популярном месте для выращивания.
- Пример использования этих классов демонстрируется созданием экземпляра pineapple (ананаса) и вызовом метода properties(), чтобы вывести информацию об ананасе, включая его свойства и популярное место для выращивания.
  
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
- Создание класс Fruit, который содержит атрибуты _name, _color, и __taste, и метод properties(), который возвращает строку, описывающую свойства фрукта.
- Создается объект apple типа Fruit, представляющий яблоко с атрибутами "Яблоко", "красный" и "сладкий".
- print(apple._name) выводит значение атрибута _name объекта apple, что будет "Яблоко".
- Однако, при попытке вывести print(apple.__tasty) возникнет ошибка, так как атрибут __taste объявлен как закрытый (private) с использованием двойного подчеркивания перед именем (__taste). Доступ к закрытым атрибутам напрямую извне класса невозможен.
  
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
- Этот код создает иерархию классов для фруктов, где Fruit является базовым классом, а Apple и Banana наследуются от Fruit.
- Каждый класс фрукта определяет метод total, который вычисляет общий вес данного вида фруктов в корзине на основе их количества.
- Создаются объекты Apple и Banana, затем они помещаются в список fruits, и в конце выводится общий вес каждого вида фруктов.

## Общие выводы по теме
- Классы позволяют создавать новые типы данных, описывая их состояние (атрибуты) и поведение (методы). Классы являются шаблонами, на основе которых можно создавать экземпляры (объекты).
- Подклассы (или дочерние классы) могут наследовать атрибуты и методы от родительских классов, расширяя их или переопределяя. Это позволяет избежать дублирования кода и повышает его повторное использование.
- Кроме того, классы и подклассы позволяют работать с полиморфизмом, что означает использование объектов разных классов через общий интерфейс.
- Использование классов и подклассов делает код более структурированным, упрощает его поддержку и понимание, позволяет создавать мощные и гибкие приложения.
