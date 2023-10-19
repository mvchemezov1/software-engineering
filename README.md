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
| Задание 6 | + |
| Задание 7 | + |
| Задание 8 | + |
| Задание 9 | + |
| Задание 10 | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
- Создайте две переменные, значение которых будете вводить через консоль. Также составьте условие, в котором созданные ранее переменные будут сравниваться, если условие выполняется, то выведете в консоль «Выполняется», если нет, то «Не выполняется».
### Код
```python
one = int(input('Введите значение первой переменной: '))
two = int(input('Введите значение второй переменной: '))
if one >= two:
    print('Выполняется')
else:
    print('Не выполняется')
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab1.png?raw=true)
### Вывод:
- Пользователь вводит два значения, которые сохраняются в переменные one и two соответственно.
- Затем выполняется условие if one >= two, которое сравнивает значения переменных one и two. Если one больше или равно two, то условие считается истинным.
- Если условие истинно, то выводится сообщение 'Выполняется'.
- Если условие ложно, то выводится сообщение 'Не выполняется'.

## Лабораторная работа №2
- Напишите программу, которая будет определять значения переменной меньше 0, больше 0 и меньше 10 или больше 10. Это нужно реализовать при помоши одной переменной, значение которой будет вводится через консоль, а также при помоши конструкций if, elif, else.
### Код
```python
one = int(input('Введите значение переменной: '))
if one < 0:
    print('Переменная меньше 0')
elif 0 < one < 10:
    print('Переменная больше 0 и меньше 10')
else:
    print('Переменная больше 10')
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab2.png?raw=true)
### Вывод:
- Строка one = int(input('Введите значение переменной: ')) предлагает пользователю ввести значение переменной и сохраняет его в переменной one, преобразуя в целое число с помощью функции int().
- Строка if one < 0: проверяет условие: если значение переменной one меньше нуля, выполняется код внутри блока if. В данном случае, если переменная меньше 0, выводится сообщение "Переменная меньше 0".
- Строка elif 0 < one < 10: проверяет второе условие: если значение переменной one больше нуля и меньше 10, выполняется код внутри блока elif. Если это условие истинно, выводится сообщение "Переменная больше 0 и меньше 10".
- Если ни одно из предыдущих условий не выполняется, то выполняется код в блоке else. В данном случае, выводится сообщение "Переменная больше 10".

## Лабораторная работа №3
- Напишите программу, в которой будет проверяться есть ли переменная
в указанном массиве используя логический оператор in.
Самостоятельно посмотрите, как работает программа со значениями
которых нет в массиве numbers.
### Код
```python
numbers = [1, 3, 4, 6, 8, 9]
value = int(input('Введите значение переменной: '))
if value in numbers:
    print('Переменная есть в данном массиве')
else:
    print('Переменной нет в этом массиве')
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab3.png?raw=true)
### Выводы:
- Создается список numbers с некоторыми числами.
- Пользователю предлагается ввести значение переменной с помощью вызова input(), и это значение преобразуется в целое число с помощью int().
- Затем код проверяет, находится ли введенное значение в списке numbers с помощью оператора in.
- Если значение присутствует в списке, выводится сообщение "Переменная есть в данном массиве".
- В противном случае выводится сообщение "Переменной нет в этом массиве".
  
## Лабораторная работа №4
-Напишите программу, которая будет определять находится ли
переменная в указанном массиве и если да, то проверьте четная она или
нет. Самостоятельно протестируйте данную программу с разными
значениями переменной value.
### Код
```python
numbers = [1, 3, 4, 6, 8, 9, 15, 16, 73, 321, 322]
value = int(input('Введите значение переменной: '))
if value in numbers:
    if value % 2 == 0:
        print('Переменная чётная и есть в данном массиве')
    else:
        print('Переменная нечётная и есть в данном массиве')
else:
    print(f"Переменная нет в массиве numbers и она равна {value}")
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab4.png?raw=true)
### Выводы:
- Данный код анализирует введенное пользователем значение переменной и проверяет его наличие в списке numbers. Если значение присутствует в списке, то дальше происходит проверка на четность.
- Если значение является четным (делится на 2 без остатка), то выводится сообщение "Переменная чётная и есть в данном массиве". В противном случае, если значение нечетное, выводится сообщение "Переменная нечётная и есть в данном массиве".
- Если введенное значение переменной не присутствует в списке numbers, то выводится сообщение "Переменная нет в массиве numbers и она равна Value ", где Value заменяется на фактическое значение переменной, введенное пользователем.

## Лабораторная работа №5
- Напишите программу, в которой циклом for значения переменной і будут меняться от 0 до 10 и посмотрите, как разные виды сравнений и операций работают в цикле.
### Код
```python
for i in range(10):
    print('i = ', i)
    if i == 0:
        i += 2
    if i == 1:
        continue
    if i == 2 or i === 3:
        print('Переменная равна 2 или 3')
    elif i in [4, 5, 6]:
        print('Переменная равна 4, 5 или 6')
    else:
        break
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab5.png?raw=true)
### Выводы:
- Сначала код печатает текущее значение i.
- Если i равно 0, к значению i добавляется 2. Однако, эта операция не влияет на весь цикл, так как в Python цикл for не видит изменения счетчика внутри цикла. Это означает, что даже если вы измените значение i внутри цикла, в следующей итерации i все равно будет увеличено на 1 от предыдущего исходного значение, а не от измененного значения.
- Если i равно 1, то с помощью команды continue цикл пропускает все остальное и переходит к следующей итерации.
- Если i равно 2 или 3, код печатает "Переменная равна 2 или 3". Здесь есть синтаксическая ошибка: тройное равенство === не существует в Python, и это должно быть изменено на ==.
- Если i равняется одному из чисел в списке [4, 5, 6], код печатает "Переменная равна 4, 5 или 6".
- Во всех остальных случаях код выходит из цикла с помощью break.

## Лабораторная работа №6
- Напишите программу, в которой при помощи цикла for определяется есть ли переменная value в строке string и посмотрите, как работает оператор else для циклов. Самостоятельно посмотрите, что выведет программа, если значение переменной value оказалось в строке string.
Определять индекс буквы не обязательно, но если вы хотите, то это делается при помоши строки:
index = string. find(value)
Вы берете название переменной, в которой вы хотите что-то найти, затем применяете встроенный метод find() и в нем указываете то, что вам нужно найти. Данная строка вернет индекс искомого объекта.
### Код
```Python
string = 'Привет всем изучающим Python!'
value = input()
for i in string:
    if i == value:
        index = string.find(value)
        print(f"Буква '{value}' есть в строке под {index} индексом")
        break
else:
    print(f"Буквы '{value}' нет в указанной строке")
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab6.png?raw=true)
### Вывод:
- Этот код Python принимает входные данные от пользователя в форме одного символа (например, буквы), и затем ищет этот символ в заданной строке (в данном случае, строка это "Привет всем изучающим Python!").
- После того как пользователь вводит значение, код начинает перебирать каждый символ в строке. Если символ, введенный пользователем, совпадает с одним из символов в строке, код находит и выводит индекс этого символа. Индекс - это позиция символа в строке (отсчет начинается с нуля). Поиск прекращается после первого совпадения.
- Если же символа, введенного пользователем, нет в строке, выводится сообщение о его отсутствии.
- Стоит учитывать что код обрабатывает строчные и заглавные букву как разные символы.

## Лабораторная работа №7
- Напишите программу, в которой вы наглядно посмотрите, как работает цикл for проходя в обратном порядке, то есть, к примеру не от 0 до 10. а от 10 до 0. В уже готовой программе показано вычитание из 100, а вам во время реализации программы будет необходимо придумать свой вариант применения обратного цикла.
### Код
```Python
value = 100
for i in range(10, -1, -1):
    value -= 1
    print(i, value)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab7.png?raw=true)
### Выводы:
- Задает начальное значение переменной value равное 100.
- Выполняет цикл, который итерируется по диапазону начиная с 10 и идет в обратном порядке до 0 (включая его) с шагом -1. Это значит, что переменная цикла i принимает значения от 10 до 0 последовательно в обратном порядке.
- В теле цикла от переменной value вычитается 1 (value -= 1).
- Затем, при каждой итерации цикла на экран выводятся два значения - значение i и value - в формате (i, value).

## Лабораторная работа №8
- Напишите программу используя цикл while, внутри которого есть какие-либо проверки, но быть осторожным, поскольку циклы while при
неправильно написанных условиях могут становится бесконечными, как указано в примере далее.
### Код
```Python
value = 0
while value < 100:
    if value == 0:
         value += 10
    elif value // 5 > 1:
        value *= 5
    else:
        value -= 5
    print(value)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab8.png?raw=true)
### Выводы:
- value = 0 вводит переменную value и задает ей начальное значение 0.
- while value < 100: устанавливает цикл, который будет выполняться до тех пор, пока value остается меньше 100.
- В цикле есть условное выражение if-elif-else:
- Если value равно 0, чтобы не возникло бесконечного цикла, value увеличивается на 10.
- Если value // 5 превышает 1 (целочисленное деление value на 5), то value умножается на 5.
- Во всех остальных случаях value уменьшается на 5.
- print(value) выводит текущее значение value на каждой итерации цикла.
- код произведет следующую последовательность действий:
     - 1) Изначально value равно 0, поэтому будет выполняться первая ветка условия, и к value прибавляется 10. Печатается число 10.
     - 2) Далее value равно 10, но 10 // 5 равно 2, что больше 1. Значит, выполнится вторая ветка условия: value умножится на 5. Печатается число 50.
     - 3) Теперь value равно 50, 50 // 5 равно 10, что больше 1, поэтому снова выполнится вторая ветка условия: value умножится на 5. Печатается число 250.
     - 4) Теперь value равно 250. 'While value  < 100' становится ложным и цикл завершается.

## Лабораторная работа №9
- Напишите программу с использованием вложенных циклов и одной проверкой внутри них. Самое главное, не забудьте, что нельзя использовать одинаковые имена итерируемых переменных, когда вы
используете вложенные циклы.
### Код
```Python
value = 0
for i in range(10):
    for j in range(10):
        if i != j:
            value += j
        else:
            pass
print(value)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab9.png?raw=true)
### Выводы:
- Данный код на языке Python выполняет двойной цикл, где каждый цикл итерируется через диапазон чисел от 0 до 9 (10 чисел всего).
- Вложенные циклы перебирают все возможные пары (i, j), где i и j изменяются от 0 до 9. Если i не равно j, то j добавляется к переменной value. Если i равно j (что равносильно паре чисел вида (0,0), (1,1), (2,2), и так далее до (9,9)), то цикл продолжает свое выполнение, не увеличивая value.
- Таким образом, сумма будет происходить по каждому диапазону от 0 до 9, исключая само число диапазона. Например, для i=0, j будет перебирать значения от 1 до 9, а для i=1, j переберет значения: 0, 2, 3, 4, 5, 6, 7, 8, 9, и так далее.
- Итоговое значение value будет равно сумме всех чисел от 0 до 9 умноженных на 9 (так как каждое число суммируется 9 раз, исключая свое собственное значение). Это даст value = 9 * (0 + 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9) = 9 * 45 = 405.
- 'pass' просто проигнорируется, когда i равны j.

## Лабораторная работа №10
- Напишите программу с использованием flag, которое будет определять есть ли нечетное число в массиве. В данной задаче flag выступает в роли индикатора встречи нечетного числа в исходном массиве, четных чисел.
### Код
```Python
even_array = [2, 4, 6, 8, 9]
flag = False
for value in even_array:
    if value % 2 == 1:
        flag = True

if flag is True:
    print('В массиве есть нечётное число')
else:
    print('В массиве все числа чётные')
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/lab10.png?raw=true)
### Выводы:
- определена переменная even_array, которая представляет из себя список чисел: 2, 4, 6, 8 и 9.
- flag объявлена как False. Этот флаг будет использоваться для отслеживания, есть ли в массиве нечетное число.
- Следующий блок кода - это цикл for, который проходит через каждый элемент в even_array.
- Внутри цикла for происходит проверка, является ли число нечетным. Это достигается путем использования оператора модуля (% 2), который возвращает остаток от деления на 2. Если число нечетное, остаток будет 1 (в данном случае value % 2 == 1 вернет True), и flag устанавливается в True.
- После того, как цикл выполнен, производится окончательная проверка: если flag равен True (или же, сказано другим способом, если он True), то печатается сообщение 'В массиве есть нечётное число'. В противном случае, когда flag все еще False, печатается сообщение 'В массиве все числа чётные'.
- В данном вводе even_array содержит одно нечетное число (9), поэтому, после выполнения кода, выводом будет 'В массиве есть нечётное число'.

## Самостоятельная работа №1
-Напишите программу, которая преобразует 1 в 31. Для выполнения поставленной задачи необходимо обязательно и только один раз использовать:
- Цикл for
- *=5
- +=1
- Никаких других действий или циклов использовать нельзя.
### Код
```python
num = 1
for _ in range(2):
    num *= 5
    num += 1
print(num)
```
### Результат
-![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind1.png?raw=true)
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
- Напишите программу, которая фразу <<Hello World>> выводит в обратном порядке, и каждая буква находится в одной строке консоли. При этом необходимо обязательно использовать любой цикл, а также программа должна занимать не более 3 строк в редакторе кода.
### Код
```python
message = "Hello World"
for i in range(len(message)-1, -1, -1):
        print(message[i])
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind2.png?raw=true)
### Выводы:
- 'message = "Hello World"' Здесь объявляется переменная message, которая содержит строку "Hello World".
- 'for i in range(len(message)-1, -1, -1):' : Здесь устанавливается цикл for. Указанная функция range() создает последовательность чисел от len(message)-1 до 0. len(message)-1 является индексом последнего символа в строке (поскольку индексы в Python начинаются с 0), и -1 является индексом, следующим за первым, что позволяет включить в последовательность и 0. Шаг -1 указывает, что каждая следующая итерация должна происходить в обратном порядке.
- 'print(message[i])' : Здесь каждый символ строки message выводится по одному, начиная с конца и идя к началу.
- Исходное сообщение выводится в обратном порядке одним символом на каждой строке.
  
## Самостоятельная работа №3
- Напишите программу, на вход которой поступает значение из консоли, оно должно быть числовым и в дилпазоне от 0 до 10 включительно (это необходимо учесть в программе). Если вводимое число не подходит по требованиям, то необходимо вывести оповешение об этом в консоль и остановить программу. Код должен вычислять в каком диапаюне находится полученное число. Нужно учитывать три диапазона
• от 0 до 3 включительно
• от 3 до б
• от б до 10 включительно
Результатом работы программы будет выведенный в консоль диапазон. Программа должна занимать не более 10 строчек в редакторе кода
### Код
```python
value = int(input("Введите число от 0 до 10: "))
if value < 0 or value > 10:
    print("Введенное значение не находится в диапазоне от 0 до 10")
    exit()
elif value <= 3:
    print("Число находится в диапазоне от 0 до 3")
elif value < 10:
    print("Число находится в диапазоне от 3 до 10")
else:
    print("Число находится в диапазоне от 10")
```
### Результат
- ![Результат1](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind3.1.png?raw=true)

- ![Результат2](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind3.2.png?raw=true)
### Выводы:
- Запрашивается ввод числа от пользователя в диапазоне от 0 до 10.
- Если введенное значение меньше 0 или больше 10, выводится сообщение "Введенное значение не находится в диапазоне от 0 до 10", а затем программа завершается.
- Иначе, если значение меньше или равно 3, выводится сообщение "Число находится в диапазоне от 0 до 3".
- Иначе, если значение меньше 10, выводится сообщение "Число находится в диапазоне от 3 до 10".
- Иначе (если значение равно 10), выводится сообщение "Число находится в диапазоне от 10".
  
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
length = len(sentence)
print("Длина предложения:", length)
lower_case = sentence.lower() # Перевод предложения в нижний регистр
print("Предложение в нижнем регистре:", lower_case)
vowels = ['a', 'e', 'i', 'o', 'u']
vowel_count = 0
for char in sentence:
        if char.lower() in vowels:
                vowel_count += 1
print("Количество гласных в предложении:", vowel_count) # Подсчет количества гласных
replaced_sentence = sentence.replace("ugly", "beauty")
print("Предложение с замененными словами:", replaced_sentence) # Замена слова "ugly" на # "beauty"
starts_with_the = sentence.startswith("The")
ends_with_end = sentence.endswith("end")
print("Начинается ли предложение с 'The':", starts_with_the)
print("Заканчивается ли предложение на 'end':", ends_with_end) # Проверка начала
# предложения с "The" и окончания на "end"
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind4.png?raw=true)
### Выводы:
- Код определяет длину предложения, используя встроенную функцию len(). Эта количество символов в предложении.
- Приводит все символы предложения к нижнему регистру с помощью метода .lower().
- Подсчитывает количество гласных букв в предложении. Цикл for проходит по каждому символу в предложении и, если этот символ присутствует в списке гласных (vowels), увеличивает счетчик вхождения гласных (vowel_count).
- Заменяет все вхождения слова "ugly" на слово "beauty" в предложении с помощью метода .replace().
- Проверяет, начинается ли предложение со слова "The" и заканчивается ли оно словом "end". Для этого используются методы строки .startswith() и .endswith().
  
## Самостоятельная работа №5
- Составьте программу, результатом которой будет вывод 'hello world' 6 раз  и 'hello' 5 раз с новой строки  чередуя друг друга в консоль:
- Программу нужно составить из данных фрагментов кода:
  -- memory = ' world'
  -- if values not in string:
  -- while ' world' not in string:
  -- string = string + ' world'
  -- if counter in value:
  -- counter = 10
  -- String = 'hello'
  -- string = memory
  -- string = ' world'
  -- counter = 0
  -- if counter > 7:
  -- print(string + memory)
  -- print(string)
  -- while counter != 10:
  -- values = [0, 2, 4, 6, 8, 10]
  -- memory = string
  -- if counter < 10:
  -- counter += 1
  -- print(memory)
  -- memory = string
- Строки кода можно использовать только один раз. Не обязательно использовать все строки кода.
### Код
```python
memory = ' world'
string = 'hello'
counter = 0
values = [0, 2, 4, 6, 8, 10]
while counter != 10:
    if counter in values:
        print(string + memory)
        print(string)
    counter += 1
string = string + ' world'
memory = string
print(memory)
```
### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_2/pic/ind5.png?raw=true)
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
