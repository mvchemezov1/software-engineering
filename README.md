# Тема 3. Операторы, условия, циклы
Отчет по Теме #3 выполнил:
- Чемезов Михаил Владимирович
- АИС-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | + |
| Задание 7 | + | + |
| Задание 8 | + | + |
| Задание 9 | + | - |
| Задание 10 | + | - |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
- Создайте две переменные, значение которых будете вводить через консоль. Также составьте условие, в котором созданные ранее переменные будут сравниваться, если условие выполняется, то выведете в консоль «Выполняется», если нет, то «Не выполняется».
### Код
```python
print(165)
print('274')
print(1.09)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab1.png?raw=true)
### Вывод:
- Данный код является простым примером вывода на экран разных типов данных.
- В первой строке кода print(165) число 165 будет выведено на экран.
- Во второй строке кода print('274') строка '274' будет выведена на экран.
- В третьей строке кода print(1.09) число 1.09 будет выведено на экран.

## Лабораторная работа №2
- Напишите программу, которая будет определять значения переменной меньше 0, больше 0 и меньше 10 или больше 10. Это нужно реализовать при помоши одной переменной, значение которой будет вводится через консоль, а также при помоши конструкций if, elif, else.
### Код
```python
print(165-28)
print(9.8 + 2.7)
print(3 + 1 + 12.78 + 2.12)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab2.png?raw=true)
### Вывод:
- Данный код выполняет математические операции и выводит результаты на экран.
- В первой строке кода print(165-28) происходит вычитание числа 28 из числа 165, и результат (137) будет выведен на экран.
- Во второй строке кода print(9.8 + 2.7) происходит сложение чисел 9.8 и 2.7, и результат (12.5) будет выведен на экран.
- В третьей строке кода print(3 + 1 + 12.78 + 2.12) происходит последовательное сложение чисел 3, 1, 12.78 и 2.12, и результат (18.9) будет выведен на экран.

## Лабораторная работа №3
- Напишите программу, в которой будет проверяться есть ли переменная
в указанном массиве используя логический оператор in.
Самостоятельно посмотрите, как работает программа со значениями
которых нет в массиве numbers.
### Код
```python
print('Привет, Мир!')

a = 'Привет, '
b = 'Мир!'
print(a + b)

world = 'Мир'
print(f"Привет, {world}!")
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab3.png?raw=true)
### Выводы:
Данный код относится к работе с текстовыми данными и строками:
- В первой строке кода print('Привет, Мир!') будет выведена на экран строка "Привет, Мир!".
- Во второй и третьей строках кода переменным a и b присваиваются значения "Привет," и "Мир!" соответственно. Затем при помощи операции сложения строк a + b, результатом будет строка "Привет, Мир!", которая будет выведена на экран.
- В четвертой строке кода переменной world присваивается значение "Мир". Затем, при использовании строки-формата через f-строку f"Привет, {world}!", будет создана новая строка "Привет, Мир!", которая будет выведена на экран.
  
## Лабораторная работа №4
-Напишите программу, которая будет определять находится ли
переменная в указанном массиве и если да, то проверьте четная она или
нет. Самостоятельно протестируйте данную программу с разными
значениями переменной value.
### Код
```python
one = 'Hello'
print(bool(one))

two = 78
print(float(two))

three = None
print(str(three))
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab4.png?raw=true)
### Выводы:
Данный код демонстрирует преобразование различных типов данных и их вывод на экран:
- В первой строке кода переменной one присваивается значение 'Hello', а затем функция bool() применяется к переменной. Функция bool() возвращает логическое значение True для любой непустой строковой переменной, поэтому в данном случае будет выведено значение True.
- Во второй строке кода переменной two присваивается значение 78, которое является целым числом. Затем функция float() применяется к переменной. Функция float() преобразует целое число в число с плавающей запятой. В данном случае будет выведено значение 78.0, уже как число с плавающей запятой.
- В третьей строке кода переменной three присваивается значение None, которое является специальным значением в Python, указывающим на отсутствие значения. Затем функция str() применяется к переменной three. Функция str() преобразует значение в строку. В данном случае будет выведено значение 'None'.

## Лабораторная работа №5
- Напишите программу, в которой циклом for значения переменной і будут меняться от 0 до 10 и посмотрите, как разные виды сравнений и операций работают в цикле.
### Код
```python
one = input('one:')
two = input('two:')
three = input('three:')
print(one, two,three)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab5.png?raw=true)
### Выводы:
- Данный код позволяет пользователю ввести значения с клавиатуры и выводит эти значения на экран.
- В первой строке кода переменной one присваивается значение, введенное пользователем с использованием функции input(). В скобках функции input() передается строка 'one:', которая будет отображаться перед ожиданием ввода значения.
- Во второй строке кода переменной two присваивается значение, введенное пользователем с использованием функции input(). В скобках функции input() передается строка 'two:', которая будет отображаться перед ожиданием ввода значения.
- В третьей строке кода переменной three присваивается значение, введенное пользователем с использованием функции input(). В скобках функции input() передается строка 'three:', которая будет отображаться перед ожиданием ввода значения.
- В четвертой строке кода функция print() используется для вывода значений переменных one, two и three на экран. Значения будут разделены пробелами.

## Лабораторная работа №6
- Напишите программу, в которой при помощи цикла for определяется есть ли переменная value в строке string и посмотрите, как работает оператор else для циклов. Самостоятельно посмотрите, что выведет программа, если значение переменной value оказалось в строке string.
Определять индекс буквы не обязательно, но если вы хотите, то это делается при помоши строки:
index = string. find(value)
Вы берете название переменной, в которой вы хотите что-то найти, затем применяете встроенный метод find() и в нем указываете то, что вам нужно найти. Данная строка вернет индекс искомого объекта.
### Код
```Python
a = 18
b = 8
print('Возведение в степень:', a ** b)
print('Обычное деление:', a / b)
print('Целочисленное деление:', a // b)
print('Нахождение остатка от деления:', a % b)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab6.png?raw=true)
### Вывод:
- Данный код выполняет математические операции с двумя переменными a и b и выводит результаты на экран.
- В первой строке кода переменной a присваивается значение 18, а переменной b присваивается значение 8.
- Во второй строке кода print('Возведение в степень:', a ** b) происходит возведение числа a в степень b, и результат будет выведен на экран.
- В третьей строке кода print('Обычное деление:', a / b) происходит деление числа a на число b, и результат будет выведен на экран.
- В четвертой строке кода print('Целочисленное деление:', a // b) происходит целочисленное деление числа a на число b, и результат будет выведен на экран.
- В пятой строке кода print('Нахождение остатка от деления:', a % b) происходит нахождение остатка от деления числа a на число b, и результат будет выведен на экран.

## Лабораторная работа №7
- Напишите программу, в которой вы наглядно посмотрите, как работает цикл for проходя в обратном порядке, то есть, к примеру не от 0 до 10. а от 10 до 0. В уже готовой программе показано вычитание из 100, а вам во время реализации программы будет необходимо придумать свой вариант применения обратного цикла.
### Код
```Python
line = 'Hello'
print(line * 6)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab7.png?raw=true)
### Выводы:
- Данный код выполняет операцию умножения со строкой и выводит результат на экран.
- В первой строке кода переменной line присваивается значение 'Hello'.
- Во второй строке кода print(line * 6) происходит умножение строки line на число 6. Это означает, что строка line будет повторена 6 раз и результат будет выведен на экран. Например, если значение line равно 'Hello', то на экран будет выведено 'HelloHelloHelloHelloHelloHello', где строка 'Hello' повторяется 6 раз.

## Лабораторная работа №8
- Напишите программу используя цикл while, внутри которого есть какие-либо проверки, но быть осторожным, поскольку циклы while при
неправильно написанных условиях могут становится бесконечными, как указано в примере далее.
### Код
```Python
sentence = 'Hello World'
print(sentence.count('o'))
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab8.png?raw=true)
### Выводы:
- Данный код подсчитывает количество вхождений символа или подстроки в строку и выводит результат на экран.
- В первой строке кода переменной sentence присваивается значение 'Hello World'.
- Во второй строке кода print(sentence.count('o')) вызывается метод count() для строки sentence с аргументом 'o', который представляет символ или подстроку, количество вхождений которого нужно подсчитать.
- Метод count() возвращает число, которое соответствует количеству вхождений символа 'o' (в данном случае) в строке sentence.
- Результат подсчета будет выведен на экран.

## Лабораторная работа №9
- Напишите программу с использованием вложенных циклов и одной проверкой внутри них. Самое главное, не забудьте, что нельзя использовать одинаковые имена итерируемых переменных, когда вы
используете вложенные циклы.
### Код
```Python
print('Hello\nWorld')
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab9.png?raw=true)
### Выводы:
- Данный код выводит на экран две строки - "Hello" и "World" - с использованием символа перевода строки ('\n').
- В коде используется функция print() для вывода текста на экран.
- Внутри функции print() передана строка 'Hello\nWorld', в которой \n используется для вставки символа перевода строки.
- Символ \n представляет собой управляющую последовательность в Python, которая обозначает переход на новую строку.
- В результате выполнения этого кода, на экране будет выведено две строки, каждая с новой строки:
- "Hello"
- "World"

## Лабораторная работа №10
- Напишите программу с использованием flag, которое будет определять есть ли нечетное число в массиве. В данной задаче flag выступает в роли индикатора встречи нечетного числа в исходном массиве, четных чисел.
### Код
```Python
sentence = 'Hello world'
print(sentence[1])
print(sentence[:5])
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab10.png?raw=true)
### Выводы:
- Данный код работает с индексами и срезами строк и выводит результат на экран.
- В первой строке кода переменной sentence присваивается значение 'Hello world'.
- Во второй строке кода print(sentence[1]) происходит обращение к символу в строке sentence по индексу 1. Индексы в строках в Python начинаются с 0, поэтому символ с индексом 1 - это второй символ строки. В данном случае будет выведен символ 'e'.
- В третьей строке кода print(sentence[:5]) происходит срез строки sentence от начала до индекса 5 (невключительно). Это означает, что будут выведены символы с индексами от 0 до 4. В результате будет выведена подстрока 'Hello'.

## Самостоятельная работа №1
-Напишите программу, которая преобразует 1 в 31. Для выполнения поставленной задачи необходимо обязательно и только один раз использовать:
- Цикл for
- *=5
- +=1
- Никаких других действий или циклов использовать нельзя.
### Код
```python
print(bool(1 < 0))
```
### Результат
-![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind1.png?raw=true)
### Выводы:
- Данный код проверяет условие "1 < 0" и выводит на экран результат проверки в виде логического значения.
- В коде используется функция bool() для приведения результата сравнения "1 < 0" к логическому типу данных.
- В данном случае условие "1 < 0" является ложным, поскольку число 1 не меньше числа 0.
- В результате выполнения кода, на экран будет выведено значение False, которое является логическим представлением ложного условия.

## Самостоятельная работа №2
- Напишите программу, которая фразу <<Hello World>> выводит в обратном порядке, и каждая буква находится в одной строке консоли. При этом необходимо обязательно использовать любой цикл, а также программа должна занимать не более 3 строк в редакторе кода.
### Код
```python
a, b, c = 1, 2, 3
print(a, b, c)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind2.png?raw=true)
### Выводы:
- Данный код присваивает значения переменным a, b и c, а затем выводит эти значения на экран.
- В первой строке кода переменным a, b и c присваиваются значения 1, 2 и 3 соответственно с помощью операции присваивания = и разделения значений запятыми.
- Во второй строке кода print(a, b, c) используется функция print() для вывода значений переменных a, b и c на экран, разделяя их пробелами.
- На экране будет выведено значение переменной a, затем значение переменной b, и наконец значение переменной c, разделенные пробелами, например: 1 2 3.
  
## Самостоятельная работа №3
- Напишите программу, на вход которой поступает значение из консоли, оно должно быть числовым и в дилпазоне от 0 до 10 включительно (это необходимо учесть в программе). Если вводимое число не подходит по требованиям, то необходимо вывести оповешение об этом в консоль и остановить программу. Код должен вычислять в каком диапаюне находится полученное число. Нужно учитывать три диапазона
• от 0 до 3 включительно
• от 3 до б
• от б до 10 включительно
Результатом работы программы будет выведенный в консоль диапазон Программа должна занимать не более 10 строчек в редакторе кода
### Код
```python
value = int(input())
if type(value) == int: print("Значение переменной:", value)
```
### Результат
- ![Результат1](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind3.1.png?raw=true)

- ![Результат2](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind3.2.png?raw=true)
### Выводы:
- Данный код считывает значение с клавиатуры в переменную value и проверяет, является ли введенное значение целым числом. Затем выводит значение переменной на экран.
- В первой строке кода происходит считывание значения с клавиатуры при помощи функции input(). Введенное значение преобразуется в целое число с помощью функции int() и присваивается переменной value.
- Во второй строке кода происходит проверка типа переменной value с помощью функции type(). Если тип переменной value равен int (целое число), то выполняется следующая инструкция.
- В третьей строке кода используется функция print() для вывода сообщения "Значение переменной:" и значения переменной value на экран.
- Если введенное значение было целым числом, то на экран будет выведено сообщение "Значение переменной:" и само значение переменной value. В противном случае, будет выведено сообщение об ошибке.
  
## Самостоятельная работа №4
- Манипулирование строками. Напишите программу на Python, которая принимает предложение (на английском) в качестве входных данных от пользователя. Выполните следующие операции и отобразите результаты:
• Выведите длину предложения
• Переведите предпожение в нижний регистр.
• Подсчитайте количество гласных (а, e, 1, o, u) в предложении.
• Замените все слова "ugly" на "beauty",
• Проверьте, начивается ли предложение с "The" и заканчивается ли на "end"
- Проверьте работу программы минимум на 3 предложениях, чтобы охватить проверку всек поставленных условий.
### Код
```python
print('конец' * 4)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind4.png?raw=true)
### Выводы:
- Данный код повторяет строку 'конец' четыре раза и выводит результат на экран.
- В коде используется функция print() для вывода текста на экран.
- Строка 'конец' умножается на число 4 с использованием оператора умножения *. Это означает, что строка 'конец' будет повторена четыре раза.
- В результате выполнения этого кода, на экран будет выведена строка 'конецконецконецконец', где строка 'конец' повторяется четыре раза.
  
## Самостоятельная работа №5
- Составьте программу, результатом которой будет данный вывод в консоль:
- Программу нужно составить из данных фрагментов кода:
- Строки кода можно использовать только один раз. Не обязательно использовать все строки кода.
### Код
```python
day, month, year = 10, 'октября', 2023
print(f"Сегодня {day} {month} {year}."+ " Всего хорошего!")
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind5.png?raw=true)
### Выводы:
- Данный код присваивает значения переменным day, month и year и затем использует эти значения для вывода текста на экран.
- В первой строке кода переменным day, month и year присваиваются значения 10, 'октября' и 2023 соответственно, с помощью операции параллельного присваивания.
- Во второй строке кода используется ф-строка (строка с префиксом f) для форматированного вывода текста на экран.
- Внутри F-строки используются фигурные скобки {} для вставки значений переменных day, month и year.
- В этом случае будет выведена строка "Сегодня 10 октября 2023. Всего хорошего!" на экран, где значения переменных day, month и year будут вставлены в соответствующие места в строке.
  
## Самостоятельная работа №6
- В предложении 'Hello World' вставьте "my" между двумя словами. Выведите полученное
предложение в консоль в одну строку. Программа должна занимать не более двух строк
редактора кода.
### Код
```python
print('Hello' + ' my ' + 'World!')
```
### Результат
- ![Резульат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind6.png?raw=true)
### Выводы:
- Данный код объединяет три строки 'Hello', ' my ' и 'World!' в одну строку и выводит результат на экран.
- В коде используется функция print() для вывода текста на экран.
- Три строки 'Hello', ' my ' и 'World!' объединяются с помощью оператора конкатенации +. Оператор + применен к строкам 'Hello' и ' my ' и затем к результату этой операции применен оператор + со строкой 'World!'.
- В результате выполнения этого кода, на экран будет выведена строка 'Hello my World!', где строки 'Hello', ' my ' и 'World!' объединены в одну строку.

  ## Самостоятельная работа №7
- Узнайте длину предложения "Hello World", результат выведите в консоль. Программа должна
занимать не более двуж строк редактора кода
### Код
```python
print(len('Hello World'))
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind7.png?raw=true)
### Выводы:
- Данный код вычисляет и выводит на экран длину строки 'Hello World'.
- В коде используется функция print() для вывода значения на экран.
- Внутри функции print() вызывается функция len(), которая вычисляет длину строки, переданной ей в качестве аргумента.
- В данном случае, строка 'Hello World' имеет 11 символов, поэтому функция len('Hello World') вернет значение 11.
- На экран будет выведено число 11, которое является результатом выполнения функции len('Hello World').

  ## Самостоятельная работа №8
- Переведите предложение HELLO WORLD' в нижний регистр. Программа должна занимать
не более друк строк редактора вода.
### Код
```python
print('Hello World'.lower())
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind8.png?raw=true)
### Выводы:
- Данный код преобразует строку 'Hello World' в нижний регистр (lowercase) и выводит результат на экран.
- В коде используется функция print() для вывода значения на экран.
- Метод .lower() применяется к строке 'Hello World', чтобы преобразовать все символы строки в нижний регистр.
- В результате выполнения этого кода, на экран будет выведена строка 'hello world', где все символы исходной строки 'Hello World' будут преобразованы в нижний регистр.

## Общие выводы по теме
- Python - мощный и простой в использовании язык программирования, который предоставляет широкий набор базовых операций для работы с данными любых типов и выполнения различных действий.
