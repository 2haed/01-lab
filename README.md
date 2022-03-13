# Лабораторная 1 - Типы данных в C++


## Вступление
Господа и господессы, мы рады приветствовать вас в нашем образовательном проекте! Надеюсь не будет обид по поводу того, что дальше мы вас будет ласково величат маслятами)

<img align="center" width="250" height="350" src="https://sun9-78.userapi.com/impg/wOu9cYnSALO1urtfJ5O_l36VzukLijqBcE77mg/d925A7hWeTk.jpg?size=670x894&quality=96&sign=cd479cc6cd58c8431844f7b280db09b9&type=album">

Поскольку вы сейчас читаете этот текст, вы для себя решили, что хотите получить, закрепить (нужное подчеркнуть) навыки программирования. Пришло время переходить к делу :ъ
Надеюсь наши дорогие маслятки уже ознакомились с **[темпланом](https://github.com/c-cpp-labs/c-cpp-labs)**, но ещё пару слов о курсе не будут лишними. Цель у данного курса лишь одна - помочь людям научиться МЫСЛИТЬ критериями программирования и в дальнейшем самим научится решать задачи, которые стоят перед ними. Тоесть грубо говоря мы довезем вас до середины реки, а дальше будем уповать на вышу смекалку и упорство. Где-то мы протяним вам палочку-выручалочку, где-то огреем ею по вашей замечательной шляпке.

<img align="center" width="500" height="350" src="https://sun9-82.userapi.com/impg/AbP1vGbSYwlwZPytZSdcEIH5nhUiy9W-JwcUsw/2MrZHMNVCwg.jpg?size=1068x830&quality=96&sign=7b7a1b1365fe81449dcaab27dd2700e6&type=album">

Одно мы можем гарантировать железно - легко не будет.

<img align="center" width="500" height="350" src="https://sun9-83.userapi.com/impg/YKIAeDXymCXOwf-04UEWmRTq59R7x5I_vO3GKw/WmjSvTCDW6g.jpg?size=604x453&quality=96&sign=059883fd29aa0758cfe81ba5ffdd97af&type=album">

Ваши находчивость, трудолюбие и желание научиться новому обязательно приведут вас к желанным навыкам и умениям, которые станут наградой за ваш нелёгкий труд и ваши страдания. К слову о страданиях, пожалуй уже пора рассказать о более конкретных вещах.
Курс не рассчитан на определённые языки ну или упоси господь один язык.

<img align="center" width="500" height="300" src="https://sun9-13.userapi.com/impg/kSJP_WPk2WdtVqSso_GAcKgtg800YoHQT01imQ/-ptcH15M4Wg.jpg?size=600x400&quality=96&sign=c3411dcdac5f57d4f5dda82772e725a6&type=album">

Ближе к середине курса вы вольны выбирать любой на ваш (самый правильный и зрящий в корень) взгляд подходящий язык программирования. Ну а чтобы хорошенько подогреть ваши стулья и смазать наших юных маслят маслом пожалуй начать стоит с великого и ужасного С++, в простонародьи "плюсы". Думаю о нем слышал даже глухой, ну а то что он "сложный", "непонятный", а так же о его высочяйщем пороге вхождения и подавно. На самом деле язык очень показательный и, уж простите за субъективность, является классикой в программировании, поскольку совмещает в себе плюсы низкоуровневости (доступ к памяти и подобные вкусняшки) а так же удобство и современность высокоуровневого языка (абстрактность).

Спасибо за внимание! А теперь от слов к делу.

<img align="center" width="500" height="300" src="https://sun9-6.userapi.com/impg/p4u7R1xXiOlm6wYJvKFjMefWChLuk5H9P1x92g/7FVSwSTZ-VE.jpg?size=1280x720&quality=96&sign=19bb0db61c94589edf36e06408263d1d&type=album">

## Теория
Итак, начнём наш курс с того, с чего обычно принято начинать любой курс по программированию - "Hello, world!"

Почему хеллоу ворлд? Да я че знаю что ли? Делать мне больше нечего узнавать почему именно нужно сначала поздороватся с миром🤔

Это база - это знать НАДААА! В общем любой уважающий себя и традиции программист начинал с этого, ну а че мы хуже что ли?

<img align="center" width="400" height="400" src="https://sun9-68.userapi.com/impg/yWBIVcCOIVo8ZGaKhW79vlPuziKygDkZimXGGA/fjnkyEf08fA.jpg?size=500x566&quality=96&sign=865c602ed10c4d9245822b8ecd42f4b2&type=album">

### Первая программа, ввод и вывод 

Чтобы не медлить, пустимся сразу же "в карьер"

Рассмотрим первую программу

```c++
#include <iostream>

int main() {
    std::cout << "Hello, world!";
    return 0;
}
```

- `#include <iostream>` - заголовок (запоминаем слово) для того, чтобы в своих программах мы могли использовать `std::cout` и `std::cin`
- `int main()` - основная функция, внутри которой будет производиться исполнение всего кода. Без этого программа попросту не будет работать
- `std::cout << "Hello, world!";` - строка, которая отвечает за вывод на экран заветного приветствия. С помощью `std::cout <<` мы можем вывести всё что угодно на консоль
- `return 0;` - строка, которая показывает операционной системе, что программа отработала хорошо. 0 - это ок, не 0 - не ок!

Напишем теперь программу, которая будет запрашивать у пользователя имя, а после - приветствовать его по имени

С миром поздоровались, опустимся на землю

```c++
#include <iostream>

int main() {
    char name[32];
    std::cout << "Enter your name: ";
    std::cin >> name;
    std::cout << "Hello, " << name << "!";
    return 0;
}
```

<img align="center" width="350" height="400" src="https://sun9-12.userapi.com/impg/cwMvWE4b5B4Yp4WAlcgHYtwr5YXK5a4JObUlCQ/lVx6nC2yk9k.jpg?size=750x1020&quality=96&sign=0dfe655663848171e3ade1f6620c98e0&type=album">

Рассмотрим новые строки
- `char name[32];` - объявление переменной, которая будет содержать имя
- `std::cout << "Enter your name: ";` - строка, которая отвечает за вывод на консоль запроса указать имя
- `std::cin >> name;` - ввод имени с консоли
- `std::cout << "Hello, " << name << "!";` - приветствие

Пока что запоминаем, каким образом выводим, каким образом вводим. Если ничего не понятно, без паники, так и должно быть.

Также обращаем внимание, что программа выполняется сверху-вниз. Сначала объявили переменную, потом её заполнили, потом вывели. Никак иначе.

А теперь к основам.

### Переменные

В языке **С++** переменная, наряду с операцией (плюс, минус, равно, умножить) - минимальная
единица языка, своего рода атом. Работая с переменными в плюсах мы имеем дело
с достаточно низкоуровневым представлением. Это определённые последовательности
бит, которые из человеческих строк и чисел переводятся в двоичные системы с помощью компилятора
и операционной системы.

Каждая переменная имеет три (или два, опционально) параметра:
```c++
int value = 10;
```
`int` - тип переменной

`value` - название переменной

`10` - начальное значение переменной (его можно не указывать)

Начнём с типов. Их существует огромное количество, среди которых:
- численные (short, int, long, float, double) - например: 10 или 10,4 
- строковые (char, string) - например: 'i' или "Никита, спасибо за курс"
- логические (bool) - True или False
- показывающие отсутствие значения (void, nullptr) - например: *ничего*

Название переменной программист обычно задаёт такое, какое его
душе угодно, но, настоятельно рекомендуется соблюдать **[правила именования 
переменных](https://github.com/bmstu-iu8-cpp/cpp-beginner-2017/blob/master/styleguide.md)** (тут вообще много всего, 
советую ознакомиться)

Переменные могут быть **инициализированы**. Это значит, что их начальное может быть задано. А может и не быть,
например
```c++
int not_initialized_value;
...
```
Переменная **объявлена**, но не **инициализирована**. При этом её значение также можно задать позднее.
```c++
...
not_initialized_value = 15;
```

### [Дальнейшее чтение по типам](https://docs.microsoft.com/ru-ru/cpp/cpp/cpp-type-system-modern-cpp?view=msvc-160)
### [Дальнейшее чтение по типам х2](https://metanit.com/cpp/tutorial/2.3.php)
(Если какие-то вещи не понятны, не паникуем. Это нормально, дойдёт позже)

### ОПЕРАЦИИ ~~(не военные)~~

Базовые операции делятся на несколько типов:
- Арифметические (+, -, *, /)
- Побитовые (|, ^, &)
- Логические (||, &&, !)
- Не арифметические (вот это да) (<<, >>, =)

Этот раздел читаем сами (надо же всё-таки воспитывать самостоятельность)

Вам помогут слова: унарность, бинарность, тернарность

### Приведение типов

<img align="center" width="350" height="400" src="https://sun9-65.userapi.com/impf/MhicBB-pJWK2Poiqg1X9JMOskFAj8QeVkaokSQ/3Umu6kAgVsM.jpg?size=600x800&quality=96&sign=fe6275c83d3a194e389368887b38bbe3&type=album">

Приведение - это от слова приводить)


Схожие типы можно приводить друг к другу. Такой процесс называется **кастом** или **кастованием**, как хотите

Рассмотрим переменную типа `long`

```c++
long big_value = 10;
```

Мы можем привести её к типу `int`

```c++
int regular_value = int(big_value);
```

Такой каст называется C-style (язык С++ произошел от языка С и наследовал почти все его механики). Он очень сильно портит вашу карму (почему - узнаете позже), поэтому стоит применять
`static_cast`

```c++
int regular_value = static_cast<int>(big_value);
```

#### Предостережение

Не стоит кастовать "большой" тип в "малый", если неизвестно достоверно, что
числа не будут выходить за рамки "малого" типа. Иначе будет как в этом меме:

<img align="center" width="350" height="400" src="https://funart.pro/uploads/posts/2021-07/1626764241_1-funart-pro-p-khomyachok-i-banan-zhivotnie-krasivo-foto-1.jpg">


Рассмотрим пример

Имеется большое число
```c++
long long very_big_value = 9000000000000000000
```

Если мы попытаемся кастануть значение этой переменной к типу инт,
получим следующую ересь

```c++
int regular_value = static_cast<int>(very_big_value); // -494665728
```

Такое происходит из-за [переполнения типов](https://etriz.ru/Chapters/TCpp/cpp003.html)


### Модификатор переменных `const`

Помимо типа при объявлении переменной можно задать дополнительные параметры, такие как `const`
```c++
const int const_value = 15;
```

Переменные с параметром `const` могут быть только **инициализированы**. Их значение по мере работы программы
не изменяется

### Структуры и кастомные типы

А теперь часть, которая дойдёт совсем не сразу

В языке С++ (и в подобных) мы можем объявлять собственные типы, наподобие int, char, etc.

При чём объявление типов происходит несколькими способами, рассмотрим их по порядку

- Присваивание alias
```c++
using size_t = unsigned long long;
```

Таким образом мы дали "прозвище" типу `unsigned long long` и можем использовать его как `size_t`

- struct

Это такой производный тип данных, который представляет абстрактную сущность
Разберём пример, чтобы сразу не закапываться в огромное количество теории

```c++
struct coordinate {
    float x;
    float y;
};
```

Данная структура представляет собой описание координаты. Любой. Это важно

А теперь создадим конкретную координату, объект этой структуры

```c++
coordinate zero{0, 0};
```

Данная переменная представляет собой начало координат. Конкретный объект типа `coordinate`, 
с которым в будущем можно будет удобно работать, как с координатой. <br/>
Получить доступ к членам этой структуры можно с помощью `.`

Выведем значение этой координаты на консоль
```c++
std::cout << "x: " << zero.x << " y: " << zero.y << '\n';
```

```shell
x: 0 y: 0
```

### CMake ~~(не тут то было)~~

В лабораторных работах мы используем системы сборки [CMake](https://habr.com/ru/post/431428/).
Данные системы сборки отличаются своей глубокой настраиваемостью и легкостью освоения.

Кстати статья обязательна по крайней мере для поверхностного ознакомления

В данных лабораторных работах файлы CMake уже написаны и настроены, поэтому
вам остаётся только творить! Удачи!

## Задание
1. Вывести на одной строке числа 1, 13 и 4221 с одним пробелом между ними.
2. Вывести на одной строке числа 1, 13 и 4221 с заданным символом между ними. Символ вводится с клавиатуры.
3. Составить программу вывода на экран в одну строку трех любых чисел с двумя пробелами между ними.
4. Дано натуральное число, выведите его последнюю цифру.
5. Дано целое неотрицательное число N, определите число десятков в нем (предпоследнюю цифру числа). Если предпоследней цифры нет, то можно считать, что число десятков равно нулю.
6. На вход дается натуральное число N. Выведите следующее за ним четное число.
7. Электронные часы показывают время в формате h:mm:ss (от 0:00:00 до 23:59:59), то есть сначала записывается количество часов, потом обязательно двузначное количество минут, затем обязательно двузначное количество секунд. Количество минут и секунд при необходимости дополняются до двузначного числа нулями. С начала суток прошло N секунд. Выведите, что покажут часы.
8. Составить программу:
   1. вычисления значения функции x=12a^2 + 7a - 12 при любом значении а; 
   2. вычисления значения функции y=3x^3 + 4x^2 - 11x + 1 при любом значении x.
9. С клавиатуры вводятся объем и масса тела. Вывести на экран плотность материала этого тела.
10. Составить программу решения линейного уравнения ax + b = 0 (a не равно 0). Числа a и b вводятся с клавиатуры.
11. Известны координаты на плоскости двух точек. Составить программу вычисления расстояния между ними. Координаты вводятся с клавиатуры.
12. Даны основания и высота равнобедренной трапеции. Найти периметр трапеции. Данные вводятся с клавиатуры.
13. Найти площадь кольца по заданным внешнему и внутреннему радиусам. Данные вводятся с клавиатуры.
14. Дана длина ребра куба. Найти объем куба и площадь его боковой поверхности. Данные вводятся с клавиатуры.
15. Дана сторона квадрата. Найти его периметр. Данные вводятся с клавиатуры.
16. Дан радиус окружности. Найти ее диаметр. Данные вводятся с клавиатуры.
17. Реализовать программу для приветствия. Имя студента вводится с клавиатуры, а на экран выводится приветствие `Hello, %name%! My name is C++.`. <br/>
18. *Дано четырехзначное число. Определите, является ли его десятичная запись симметричной. Если число симметричное, то выведите 1, иначе выведите любое другое целое число. Число может иметь меньше четырех знаков, тогда нужно считать, что его десятичная запись дополняется слева незначащими нулями. 

## Условия приёма работы
* выполнить все задания в ветке `work`;
* Код должен проходить проверку сборки в GitActions;
