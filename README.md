# Лабораторные работы

- [Семестр 1](#семестр-1)
  - [Лабораторная 8](#лабораторная-8---функции-обработки-текста)
  - [Лабораторная 9](#лабораторная-9---структуры)
- [Семестр 3](#семестр-3)
  - [Лабораторная 1](#лабораторная-1)

---

# Семестр 1

### Требования к подготовке:

Необходимы начальные знания о библиотеке стандартного ввода/вывода (подключаемый заголовочный файл – `stdio.h`) в части работы с целыми и вещественными числами.  Знание циклов и указателей.
Для вычисления математических операций использовать заголовочный файл `math.h`. 

### Требования к программе:
1. Программа компилируется, запускается и выводит правильный результат.
2. В программах организован понятный для пользователя ввод/вывод (при запросе исходных данных соответствующий запрос должен выводиться на экран на литературном русском или английском языке с соблюдением правил написания; все пробелы, знаки препинания и пр. должны быть на месте; использование транслита запрещено).
3. Строка представляет из  себя массив символов и имеет тип `char*`.
4. Класс `String` использовать нельзя.
5. Результат выполнения функции вывести на экран в функции `main()`.
6. Внутри функции обработки строки не должно быть использовано функций ввода или вывода. Вся работа с консолью должна находиться в функции `main()`.
7. Ваша функция не должна возвращать `void`.

## Лабораторная 8 - Функции обработки текста

### Задание №1

Пусть во входном потоке находится последовательность литер, заканчивающаяся точкой (кодировка `ASCII`):

Выяснить, есть ли среди символов этой последовательности символы, образующие слово ***char***.

### Задание №2

Пусть во входном потоке находится последовательность литер, заканчивающаяся точкой (кодировка `ASCII`). Вывести в выходной поток последовательность литер, измененную следующим образом:

Удалить все комбинации символов ***the***;

## Лабораторная 9 - Структуры

1. Описать структуру с именем `NOTE`, содержащую следующие поля:
- `NAME` - фамилия, имя;
- `TELE` - номер телефона;
- `BDAY` - день рождения (массив из трех чисел).
2. Написать программу, выполняющую следующие действия:
- Ввод с клавиатуры данных в массив `BLOCKNOTE`, состоящий из элементов типа `NOTE`; записи должны быть упорядочены по трем первым цифрам номера телефона;
- Вывод на экран информации о человеке, чья фамилия введена с клавиатуры;
- Если такого нет, выдать на дисплей соответствующее сообщение.

# Семестр 3

## Лабораторная 1

### Общая часть заданий

Написать программу, демонстрирующую работу с объектами двух типов: `Т1` и `Т2`, для чего создать систему соответствующих классов. Каждый объект должен иметь идентификатор (в виде произвольной строки символов) и одно или несколько полей для хранения состояния объекта (один класс является потомком другого). Клиенту (функции `main()`) должны быть доступны следующие основные операции (методы): создать объект, удалить объект, показать значение объекта и прочие дополнительные операции (зависят от варианта). Операции по созданию и удалению объектов инкапсулировать в классе `Factory`., Предусмотреть меню, позволяющее продемонстрировать заданные операции.

При необходимости в разрабатываемые классы добавляются дополнительные методы (например, конструктор копирования, операция присваивания и т. п.) для обеспечения надлежащего функционирования этих классов.

В таблице 1 и 2 перечислены возможные типы объектов и возможные дополнительные операции над ними. Здесь и далее в таблице рассматриваются только целые положительные числа.

#### Таблица 1. Перечень типов объектов

| Класс        | Объект                                                          |
| :---         | :----                                                           |
| `SymbString` | Символьная строка (произвольная строка символов)                |
| `BinString`  | Двоичная строка (изображение двоичного числа)                   |
| `OctString`  | Восьмеричная строка (изображение восьмеричного числа)           |
| `DecString`  | Десятичная строка (изображение десятичного числа)               |
| `HexString`  | Шестнадцатеричная строка (изображение шестнадцатеричного числа) |

#### Таблица 2. Перечень дополнительных операций (методов)

| Операция (метод) | Описание |
| :---             | :----    |
| `ShowBin()`           | Показать изображение двоичного значения объекта |
| `ShowOct()`           | Показать изображение восьмеричного значения объекта |
| `ShowDec()`           | Показать изображение десятичного значения объекта |
| `ShowHex()`           | Показать изображение шестнадцатеричного значения объекта |
| `operator+(T&, T&)`   | Для объектов `SymbString` — конкатенация строк; для объектов прочих классов — сложение соответствующих численных значений с последующим преобразованием к типу `Т` |
| `operator-(T&, T&)`   | Для объектов `SymbString` — если **s2** содержится как подстрока в **s1**, то результатом является строка, полученная из **s1** удалением подстроки **s2**; в противном случае возвращается значение **s1**; для объектов прочих классов — вычитание соответствующих численных значений с последующим преобразованием к типу `Т` |

#### Варианты

| Номер | T1           | T2          | Операция (метод)    |
| :---  | :----        | :---        | :---                | 
| 9     | `SymbString` | `HexString` | `operator+(T&, T&)` |
