# Задание 2 для курса "Программирование на языке Python"

# Знакомство с Git

## Задача 2.1

Дана папка [wild_animals](wild_animals.zip), в которой хранятся файлы свежесозданного блога о диких животных. Файловая структура данной директории:

```console
wild_animals
  ├── index.html
  └── pictures
    ├── elephant.jpg
    ├── giraffe.jpg
    └── paw_print.jpg
```

Как видно из структуры, в корневой директории лежат:
1. Основная страница блога index.html
2. Папка pictures, в которой хранятся изображения ( файлы *.jpg) сайта

В ходе задания будет необходимо создать на основе директории wild_animals репозиторий Git и внести в него некоторые изменения, после чего зафиксировать их средствами Git.

### Условие задачи

1. Создайте репозиторий внутри папки wild_animals. Убедитесь, что внутри папки wild_animals появилась папка .git.

2. Настройте пользователя Git на уровне репозитория wild_animals:
    1) Изучите содержимое файла конфигурации Git для текущего репозитория (.git/config)
    2) Настройте имя и email пользователя для текущего репозитория
    3) Убедитесь, что файл .git/config изменился соответствующим образом

3. Изучите содержимое папки .git/objects
    1) Убедитесь, что отсутствует файл индекса (.git/index)
    2) Убедитесь, что папка с объектами Git пустая (.git/objects)
    3) Убедитесь, что указатель HEAD указывает на ветку main

4. Сделайте 1й коммит:
    1) Сделайте файлы папки wild_animals отслеживаемыми
    2) Обратите внимание на файл индекса (.git/index) и папку с объектами (.git/objects)
    3) Сделайте коммит
    4) Найдите хэш коммита

5. Сделайте 2й коммит
    1) Исправьте опечатку в файле index.html (опечатка в слове Elephant)
    2) Добавьте изменения в индекс
    3) Сделайте коммит

6. Сделайте 3й коммит
    1) Добавьте в файл index.html секцию для еще одного животного (например, для кенгуру)
    2) Добавьте изменения в индекс
    3) Сделайте коммит

## Задача 2.2

Дана маленькая библиотека, вычисляющая некоторые тригонометрические функции. Она имеет следующую структуру:

**Структура директории mat_lib**
```console
mat_lib
    ├─docs
    │   └─math_lib_docs.txt
    │
    └─pyfiles
        └─factorial.py
        └─test.py
        └─trigonometry.py
```

Назначение каждого из файлов:
1. `[ math_lib_docs.txt ]` Короткая документация по функционалу библиотеки
2. `[ factorial.py ]` Модуль с функцией factorial(), которая вычисляет факториал переданного числа
3. `[ trigonometry.py ]` Модуль с тригонометрическими функциями, например, sin()
4. `[ test.py ]` Модуль для проверки функционала тригонометрических функций для разных значений углов

### Условие задачи

1) Инициализируйте репозиторий в папке mat_lib

2) Задайте имя пользователя и email глобально
    1. Проверьте, что изменения внесены в файл глобальных настроек .gitconfig
    2. Проверьте, что файл локальных настроек .git/config не был изменен

3) Изучите содержимое папки .git/
    1. Узнайте, на что сейчас указывает HEAD
    2. Просмотрите файл, на который указывает HEAD (в этом пункте есть подвох)

4) Добавьте все файлы в индекс

5) Сделайте первый коммит
    1. Просмотрите объект коммита, найдите хэш объекта-дерева корня репозитория
    2. Просмотрите объект дерева корня репозитория
    3. Проверьте, на что указывает HEAD сейчас
    4. Просмотрите файл, на который указывает HEAD
    5. Ответьте на вопрос: на что указывает текущая ветка? Для этого просмотрите на объект, на который указывает ветка.

6) Выполните файл test.py
    1. Просмотрите статус файлов, чтобы обнаружить, что появились файлы кэша

7) Сделайте второй коммит
    1. Просмотрите объект коммита, найдите хэш родительского коммита
    2. Посмотрите, на что сейчас указывает HEAD
    3. Проверьте файл, на который указывает HEAD 
    4. Узнайте, на что указывает текущая ветка. Для этого просмотрите на объект, на который указывает ветка.

## Задача 2.3

Дана библиотека, написанная на Python - Geometric Lib. Файловая структура данной библиотеки:

**Структура папки geometric_lib**
```console
geometric_lib
    ├── circle.py
    ├── square.py
    └── docs
         └── README.md
```
В качестве задания необходимо выполнить ряд действий над репозиторием geometric_lib: создадим новую ветку, сделаем коммиты, посмотрим историю и изучим внесенные изменения средствами Git.

### Условие задачи

1) Выполните команду git clone https://github.com/Zernovs-courses/geometric_lib.git.
Она скопирует репозиторий к вам на компьютер.

2) Создайте новую ветку с названием new_features и переключитесь на нее.

3) Добавьте новый файл в эту ветку. 
Например, с вычислениями для фигуры Прямоугольник. 
Его название: rectangle.py
Его содержимое:

```python
def area(a, b): 
    return a * b 

def perimeter(a, b): 
    return a + b 
```

4) Сделайте коммит с сообщением `"L-03: Added rectangle.py"`.

5) Добавьте еще один файл в эту ветку. 
Например, с вычислениями для фигуры Треугольник.
Его название: triangle.py
Его содержимое:

```python
def area(a, h): 
    return a * h / 2 

def perimeter(a, b, c): 
    return a + b + c 
```

6) Исправьте ошибку в вычислении периметра в файле rectangle.py, 
теперь он должен стать таким:

```python
def area(a, b): 
    return a * b 

def perimeter(a, b): 
    return 2 * (a + b) 
```

7) Создайте еще один коммит внутри этой же ветки, его сообщение:
`"L-03: Added triangle.py and fixed rectangle perimeter bug"`.

8) Постройте граф истории всего репозитория с однострочным выводом коммитов.

9) Постройте граф истории только текущей ветки. 
В ней должно быть два последних коммита.

10) Возьмите хэши двух последних коммитов из истории и посмотрите, 
какие изменения были внесены.

11) Обычно, так не делают на практике, но мы только учимся, 
поэтому давайте удалим ветку new_features без слияния. 
Не забудьте, что нельзя удалить ветку, на которой находится HEAD.

