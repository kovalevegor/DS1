# Лекция 1. Техника работы

#### 1. В этом задании требуется научиться использовать компилятор C++ из командной строки или некоторого файлового менеджера.

* Напишите программу A + B на C++ в редакторе Far Manager. Можно использовать любой базовый текстовый редактор
* Выполните трансляцию программы из командной строки. Для упрощения работы можно использовать bat-файл
* Запустите программу из командной строки и проверьте ее работоспособность
* В отсчет вставьте текст программы и команды ее трансляции и запуска
```
Внимание. При проверке этого зания вам необходимо будет проедлать все эти действия в аудиториию При этом будет учитываться время выполнения задания. Задание будет засчитано, если время его выполнения не превысит две минуты
```


#### 2. Для используемого вами транслятора подготовьте список основных опций трансляции. В него обязательно должны входить следующие опции: оптимизация кода, выбора стандарта языка, работы с предупреждениями и другие, которые покажутся вам важными. Сделайте краткое описание этих опций. 



#### 3. Напишите программы с использованием особенностей С++11 и С++17. Выполните их трансляцию с указанием стандарта языка. Запустите эти программы и проверьте их работоспособность. Для С++11 можно использовать инициализации, например: 

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

#### 4. В следующих заданиях потребуется сравнить время работы алгоритмов сортировки на С++ и других языках. Для этого потребуется приготовить тесты. Каждый тест будет последовательностью целых чисел. Каждый файл будет содержать несколько тестов. Все тесты будут разбиты на группы по длине. Все тесты одной группы имеют одинакомую длину. Будет использоваться следующий формат файла: в файле в первой строке надо записать количество групп тестов. Далее количество тестов в первой группе и длина тестов. Далее через пробел сами тесты, по одному тесту в каждой строкею После этого аналогично описание второй группы тестов и так далее. Например:

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


#### 5.
#### 6. 
### 7. 
### 8.
