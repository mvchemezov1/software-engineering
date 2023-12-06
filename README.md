# Итоговый проект
Отчет по Итоговому_проекту выполнил:
- Чемезов Михаил Владимирович
- АИС-21-1

| Задание | Сам_раб |
| ------ | ------ |
| Итоговый проект | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Тема итогового проекта: крестики-нолики на python
Я реализовал игру "крестики-нолики" на python с помощью полученных знаний на дисциплине "Программная инженерия"
### Код
```python
class TicTacToe:
    def __init__(self):
        self.board = [' ' for _ in range(9)]  # Инициализация доски 3х3 пустыми ячейками
        self.current_winner = None  # Победитель игры (None - пока нет победителя)

    def print_board(self):
        for row in [self.board[i*3:(i+1)*3] for i in range(3)]:
            print('| ' + ' | '.join(row) + ' |')  
        # Вывод доски в виде трех строк, разделенных вертикальными полосами

    @staticmethod
    def print_board_nums():
        number_board = [[str(i) for i in range(j*3, (j+1)*3)] for j in range(3)]
        for row in number_board:
            print('| ' + ' | '.join(row) + ' |')  
        # Вывод номеров клеток на доске для удобства игрока при выборе хода

    def available_moves(self):
        return [i for i, spot in enumerate(self.board) if spot == ' ']
        # Возвращает список доступных ходов (индексов пустых клеток)

    def empty_squares(self):
        return ' ' in self.board
        # Проверяет, есть ли пустые клетки на доске

    def num_empty_squares(self):
        return self.board.count(' ')
        # Возвращает количество пустых клеток на доске

    def make_move(self, square, letter):
        if self.board[square] == ' ':
            self.board[square] = letter  # Совершение хода игроком или компьютером
            if self.winner(square, letter):  # Проверка, если этот ход приводит к победе, то:
                self.current_winner = letter  # Устанавливаем текущего победителя
                return True
        return False

    def winner(self, square, letter):
        row_ind = square // 3  # Вычисляем индекс строки клетки хода
        row = self.board[row_ind*3:(row_ind+1)*3]  # Получаем строку, содержащую клетку, в которую был сделан ход
        if all([spot == letter for spot in row]):
            return True  # Все клетки в строке равны ходу игрока, значит он победил

        col_ind = square % 3  # Вычисляем индекс столбца клетки хода
        column = [self.board[col_ind+i*3] for i in range(3)]  # Получаем столбец, содержащий клетку, в которую был сделан ход
        if all([spot == letter for spot in column]):
            return True  # Все клетки в столбце равны ходу игрока, значит он победил

        if square % 2 == 0:  # Если клетка находится на диагонали
            diagonal1 = [self.board[i] for i in [0, 4, 8]]  # Получаем диагональ, содержащую клетку, в которую был сделан ход
            if all([spot == letter for spot in diagonal1]):
                return True  # Все клетки на диагонали равны ходу игрока, значит он победил

            diagonal2 = [self.board[i] for i in [2, 4, 6]]  # Получаем вторую диагональ
            if all([spot == letter for spot in diagonal2]):
                return True  # Все клетки на второй диагонали равны ходу игрока, значит он победил

        return False  # Если ни одно из условий не выполнилось, значит игрок не победил


def play_game():
    x_player = 'X'  # Инициализация игрока X
    o_player = 'O'  # Инициализация игрока O

    t = TicTacToe()  # Создание экземпляра класса TicTacToe

    while t.empty_squares():  # Пока на доске есть пустые клетки
        t.print_board_nums()  # Вывод номеров клеток на доске

        if t.num_empty_squares() == 1:  # Если осталась одна пустая клетка
            move = t.available_moves()[0]  # Получение доступного хода
        else:
            try:
                move = int(input("Введите число для вашего хода (0-8): "))  # Ввод хода игрока X
            except ValueError:
                print("Некорректный ввод. Попробуйте еще раз.")
                continue
            if move not in t.available_moves():
                print("Это поле уже занято. Попробуйте еще раз.")
                continue

        t.make_move(move, x_player)  # Выполнение хода игрока X
        if t.current_winner:  # Если есть победитель
            t.print_board()
            print(f"{t.current_winner} выиграл!")
            break

        t.print_board()
        if t.num_empty_squares() == 0:  # Если нет доступных ходов
            print("Ничья!")
            break

        move = int(input("Введите число для вашего хода (0-8): "))  # Ввод хода игрока O
        t.make_move(move, o_player)  # Выполнение хода игрока O

        if t.current_winner:  # Если есть победитель
            t.print_board()
            print(f"{t.current_winner} выиграл!")
            break

    if not t.empty_squares() and not t.current_winner:  # Если нет доступных ходов и нет победителя
        print("Ничья!")


play_game()  # Запуск игры
```

### Результат
- ![Результат](https://github.com/mvchemezov1/software-engineering/blob/%D0%A2%D0%B5%D0%BC%D0%B0_11/pic/Lab1.png)
### Вывод:
- Создание класса TicTacToe:
- Класс TicTacToe инициализирует игровую доску размером 3х3 и переменную current_winner, которая пока равна None.
- Метод print_board отображает текущее состояние игровой доски. Он использует цикл для печати каждой строки доски, разделенной вертикальными полосами "|".
- Статический метод print_board_nums выводит номера клеток на доске для удобства игрока при выборе хода. Он использует цикл для создания списка номеров клеток и печатает их, разделенные вертикальными полосами "|".
- Метод available_moves возвращает список доступных ходов. Он использует генератор списка, чтобы получить индексы пустых клеток на доске.
- Метод empty_squares проверяет, есть ли пустые клетки на доске. Он возвращает True, если есть хотя бы одна пустая клетка, и False в противном случае.
- Метод num_empty_squares возвращает количество пустых клеток на доске. Он использует метод count для подсчета количества пустых клеток в списке доски.
- Метод make_move делает ход игрока в указанную клетку доски. Он принимает параметры square (индекс клетки) и letter (ход игрока).
- Если клетка пустая, то она заполняется ходом игрока.
- Метод также проверяет, победил ли игрок после этого хода, с помощью метода check_win.
- Если игрок победил, то метод возвращает True, в противном случае - False.
- Метод check_win проверяет, победил ли игрок после последнего хода. Он проверяет все возможные комбинации выигрышных полей (3 в ряд по горизонтали, вертикали и диагоналям).
- Если какая-либо комбинация равна ходу игрока, то игрок победил и метод возвращает True.
- В противном случае, метод возвращает False.
