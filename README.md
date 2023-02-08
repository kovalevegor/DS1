# Лекция 1. Техника работы

#### 1. В этом задании требуется научиться использовать компилятор C++ из командной строки или некоторого файлового менеджера.

* Напишите программу A + B на C++ в редакторе Far Manager. Можно использовать любой базовый текстовый редактор
* Выполните трансляцию программы из командной строки. Для упрощения работы можно использовать bat-файл
* Запустите программу из командной строки и проверьте ее работоспособность
* В отсчет вставьте текст программы и команды ее трансляции и запуска
```
Внимание. При проверке этого зания вам необходимо будет проедлать все эти действия в аудиториию При этом будет учитываться время выполнения задания. Задание будет засчитано, если время его выполнения не превысит две минуты
```
##### Сборка
Для сборки программы необходимо указать компилятору g++ файлы исходного кода, например команда g++ ```main.cpp``` скомпилирует исходный код файла ```main.cpp``` в исполняемый фаил ```a.out``` *(если компилятору не указать имя выходного файла то по умолчанию именем будет ```a.out```)*

```-o <name>``` - Имя выходного файла

**Пример:** Команда ```g++ -o myexe``` ```main.cpp``` скомпилирует фаил ```main.cpp``` в исполняемый фаил ```myexe```.

Можно передавать несколько исходных файлов для сборки, например ```g++ -o myexe``` ```file1.cpp file2.cpp```.

-c - Создание объектного файла

**Пример:** Для создания объектного файла необходимо указать компилятору ключи ```-c и -o: g++ -c -o main.o``` ```main.cpp```, данной командой компилятор ```g++``` создает объектный фаил main.o из файла ```main.cpp```

Для сборки программы из объектных файлов необходимо указать компилятору в качестве входных параметров не файлы исходного кода а объектные файлы: ```g++ -o myexe``` foo.o main.o bar.o - создает программу из объектных файлов foo.o main.o bar.o

-I<include_path> - Указание каталога для поиска подключаемых файлов

**Пример:** ```g++ -o myexe``` ```-I/my/path/to/include ``````main.cpp```

```-L<library_path>``` - Указание каталога для поиска библиотек

```-l<library>``` - Указание конкретной библиотеки для линковки

#### 2. Для используемого вами транслятора подготовьте список основных опций трансляции. В него обязательно должны входить следующие опции: оптимизация кода, выбора стандарта языка, работы с предупреждениями и другие, которые покажутся вам важными. Сделайте краткое описание этих опций. 



#### 3. Напишите программы с использованием особенностей С++11 и С++17. Выполните их трансляцию с указанием стандарта языка. Запустите эти программы и проверьте их работоспособность. Для С++11 можно использовать инициализации, на**пример:** 

```cpp
std::cin >> a >> b >> c;
std::cout << std::min({a,b,c});
```

Для С++17 можно использовать инстанцирование шаблона класса по конструктору.

```cpp
std::cin >> a >> b >> c;
std::vector v = {a, b, c};
for (auto x:v)
    std::cout << x << ' ';
```

В отчет вставьте полные тексты программ и команды для их трансляции и запуска.

#### 4. В следующих заданиях потребуется сравнить время работы алгоритмов сортировки на С++ и других языках. Для этого потребуется приготовить тесты. Каждый тест будет последовательностью целых чисел. Каждый файл будет содержать несколько тестов. Все тесты будут разбиты на группы по длине. Все тесты одной группы имеют одинакомую длину. Будет использоваться следующий формат файла: в файле в первой строке надо записать количество групп тестов. Далее количество тестов в первой группе и длина тестов. Далее через пробел сами тесты, по одному тесту в каждой строкею После этого аналогично описание второй группы тестов и так далее. На**пример:**

```txt
3                   // количество групп тестов
2 5                 // первая группа. два теста по 5 чисел
1 2 3 4 5           // первый тест
5 4 3 2 1           // второй тест
2 8                 // вторая группа тестов. два теста по 8 чисел
5 1 2 8 3 10 4 7
8 1 7 2 4 3 6 5 
2 3                 // третья группа. два теста по 3 числа
1 3 2 
9 10 11 
```
#### Вы должны написать программу на языке С++, которая будет генерировать такие файлы. Программа должна использовать библиотеку testlib.h. На вход программе подаются: имя файла, строка инициализации биьблиотеки (для вызова функции setName()), количество групп тестов, количество тестов в каждой группе, последовательность длин тестов в каждой группе, диапазон случайных чисел для теста. Программа должна читать все эти параметры из текстового файла pfrfm.txt. Для генерации требуется реализовать алгоритм генеации различных случайных чисел. Для ускорения вывода следует обязательно отключить синхронизацию потоков и использовать иптимизацию кода по времени. Программы с медленной генерацией тестов не будут проверяться. 

#### 5. В этом задании вам надо будет написать программу для выполнения сотировки последовательности целых чисел в С++ разными способами. Их достаточно много. Выберем пять следующих способов. 

* sort
* stable sort
* sort heap
* при помощи set. Заносим все числа из вектора в set, а потом возвращаем обратно. Способ работает только для различных чисел. Например, пусть значения лежать в векторе V:

```cpp
set<int> S(V.begin(), V.end()):
copy(S.begin()m, S.end(), V.begin());
```
* Сортировка связанного списка. Заносим все числа из вектора в связный список, сортируем из там при помощи метода сортировки списка, возвращаем обратно.

```cpp
list<int> L(V.begin(), V.end());
L.sort();
copy(L.begin(), L.end(), V.begin());
```
Ваша программа должна работать следующим образом. 

* Для каждого способа сортировки надо написать функцию которая его реализует, например

```cpp
double srt1(vector <int> V) {
    ...
}
```
    Обратите внимание, что вектор передается по значению. Как правило, вектора передаются по ссылке, но здесь передача по значению нужна, чтобы каждый раз выполнять сортировку заново для измерения времени. Функция должна запоминать текущее время, вызвать один из методов сортировки и вернуть разницу между текущим временем в момент завершения сортировки и запомненным. 

* Создаем и открываем для записи текстовый файл protocol.txt 
* Из файла читаем количесвто тестов в группе и длину теста. Создаем вектор требуемой длины. Делаем цикл по количеству тестов в группе. 
* Читаем числа и файла в вектор
* Для каждого метода сортировки запускаем функцию этого метода *три раза* и находим минимум из возвращенных значений. Запоминаем этот минимум. 
* После завершения цикла по группе тестов находим среднее арифметическое из запомненных минимумов для каждого метода сортирвки. Выводим в файл protocol.txt строку из 6 чисел: длина теста в группе и среднее арифметическое для каждого метода сортировки 

При написании прогрммы следует обязательно отключать синхронизацию потоков и использовать оптимизацию кода по времени. 

#### 6. Используя программы из предыдущих заданий, определите, вектор какой размера сортируется на вашем компьютере примерно за секунду. Для этого сделайте тестовый файл из одной группы тестов. В группе должно быть пять тестов некоторой длины *m*. Подберите это число так, чтобы среднее время работы саного быстрого метода сортивовки в файле protocol.txt равнялось примерной одной секунде. Будет достаточно, если число *m* будет округлено до 100000, то есть число будет оканчиваться на 5 нулей. В отчете запишиет, какие длины тестов вы пробовали и какое время работы получили. 

#### 7. Используя программы из предыдущих заданий и найденное ранее число *m*, создайте тестовый файл из 10 групп тестов. В каждой группе должно быть по три теста с длинами равными *0:2m, 0:4m, 0:6m, 0:8m, m, 1:2m, 1:4m, 1:6m, 1:8m, 2m*. Проверьте время сортировки на этих группах тестов. В отчет запишите данне из файла protocol.txt

#### 8. 


#### 9.
#### 10.
#### 11.
#### 12.
