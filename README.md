# Требования

* Все работы необходимо загрузить в этот репозиторий.
* Все работы должны быть быть написаны в рамках стандарта C++14.
* Работы необходимо размещать в собственном каталоге с названием в формате `<фамилия>.<имя>`, набранным строчными латинскими символами (например `ivanov.ivan`).
* Каждая работа должна быть в отдельном каталоге с соответствующим названием:
  * `T0` - пробная (здесь и далее буква T латинская)
  * `T2` - задание 1, потоки и итераторы (номер 2 - не опечатка)
  * `T3` - задание 2, алгоритмы
* Каждую работу необходимо выполнять в собственной ветке Git с названием `<фамилия>.<имя>/<работа>` (`ivanov.ivan/T0`).
* Для того, чтобы работа была принята, необходимо создать pull request. На каждую работу должен быть создан свой pull request и при том только один!
* Каждый коммит должен обладать комментарием, из которого понятно, что и зачем было сделано.
* Длина строк не должна превышать 100 символов.
* Для отступов должны использоваться только пробелы, не табуляции! (Для VisualStudio Tools → Options → Text Editor → [язык] → Tabs → Insert spaces)
* Окончания строк и конца файла должны быть в unix-style, последним символом в каждом файле должен быть символ перевода строки.
  Те, кто использует Git в Windows, могут установить указанную ниже настройку или выбрать соответствующий пункт при установке [(руководство)](https://git-scm.com/book/ru/v2/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-Git-%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D1%8F-Git)
```
  git config --global core.autocrlf true
```
* Вывод каждой работы должен заканчиваться переводом курсора на новую строку.
* Работы должны сдаваться по порядку (см. файл .config в корне репозитория).

# Пробная работа T0

Реализуйте программу, которая выводит в стандартный вывод на отдельной строке ваши фамилию и имя, разделенные точкой:
```
ivanov.ivan
```

# Порядок отправки работ

Далее приведены некоторые команды на Bash (консоль Git Bash для Windows устанавливается вместе с Git)

### Git

* Скачайте и установите Git на свой компьютер [с сайта](https://git-scm.com/downloads) или через [менеджер пакетов](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git).
* [Настройте Git](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%9F%D0%B5%D1%80%D0%B2%D0%BE%D0%BD%D0%B0%D1%87%D0%B0%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-Git).
* Вы можете установить [графический интерфейс](https://git-scm.com/downloads/guis), например SourceTree, или воспользоваться средствами, встроенными в IDE.
* [Учебник](https://git-scm.com/book/ru/v2)

### Подготовка собственного репозитория

1. Сделайте fork репозитория средствами GitHub
2. Получите локальный репозиторий (git clone):
```
  cd <путь до каталога, где вы хотите разместить репозиторий>
  git clone <ссылка на fork>
```
3. Перейдите в каталог с локальным репозиторием:
```
  cd <локальный репозиторий>
```
4. Добавьте основной репозиторий в список удалённых (remote):
```
  git remote add upstream https://github.com/ilya-shemyakin/30002.git
```
5. Проверьте, что локальный репозиторий связан с вашим и с основным удалёнными репозиториями:
  * `git remote get-url origin` – должна быть ссылка на **ваш fork**
  * `git remote get-url upstream` – должна быть ссылка на **основной репозиторий**

### Начало выполнения каждой работы

1. Переключиться на master-ветку:
```
  git checkout master
```
2. Создать новую ветку с необходимым названием от master-ветки в **локальном** репозитории и переключиться на нёё:
```
  git checkout -b ivanov.ivan/T0
```
3. Создать папку для новой работы. Сделать это можно разными способами, в т.ч. и через IDE, но отправлять на проверку файлы, созданные IDE **не нужно**.
4. Создать main.cpp, содержащий компилирующуюся функцию `main()` и добавить его в Git:
```
  git add ivanov.ivan/T0/main.cpp
```
5. Cоздать коммит:
```
  git commit -m "Initial commit for T0"
```
6. Создать ветку в своём удалённом репозитории (fork) и отправить первую версию работы туда:
```
  git push -u origin ivanov.ivan/T0
```

### Дальнейшее выполнение работы

1. Добавить изменённые файлы в Git:
```
  git add <имя файла>
```
2. Создать новый коммит:
```
  git commit -m "<сообщение>"
```
3. отправить изменения в свой удалённый репозиторий (fork):
```
  git push
```
Все эти шаги вы можете проделать и через графический интерфейс.

### Создание pull request

После отправки готовой работы в свой удалённый репозиторий (fork), необходимо отправить её на проверку в основной репозиторий. Для этого средствами GitHub создайте pull request из соответствующей ветки fork'а в master ветку основного репозитория.

Также для проверки выполнения тестов можно создать pull request в master ветку fork'а, **но принимать (merge) этот pull request не следует**! Для активации тестов необходимо нажать кнопку "Enable..." на странице Actions.

### Синхронизация с основным репозиторием

Работы должны сдаваться по порядку. После того, как ваш pull request принят (merge) в основном репозитории, необходимо синхронизировать master-ветки fork и основного репозитория:
1. Переключиться на master-ветку в **локальном** репозитории:
```
  git checkout master
```
2. Скачать метаданные Git из **основного** репозитория:
```
  git fetch upstream
```
3. Объединить изменения из master **основного** репозитория в master **локального**:
```
  git merge upstream/master
```
4. Отправить изменения master **локального** репозитория в **свой удалённый (fork)**:
```
  git push
```
Если в этот момент вы уже выполняете следующую работу в другой ветке, то необходимо добавить в неё изменения из **локальной** ветки master:

5. Переключиться на ветку с лабораторной:
```
  git checkout -b ivanov.ivan/T2
```
6. Синхронизировать рабочую ветку с **локальной** веткой master
```
  git merge master
```
7. Синхронизируем изменения в **локальной** ветке с соответствующей веткой в **своём удалённом (fork)** репозитории
```
  git push
```

# Сборка и тестирование работ

* На проекте используется Continuous Integration (CI), соответственно, сборка и тестирование выполняются автоматически. Коммиты, не прошедшие CI (с ошибкой или пропустившие CI) не принимаются.
* Для сборки и запуска работ присутствует Makefile для [GNU Make](https://www.gnu.org/software/make/).
* Файл "main.cpp" особенный: его назначение - функция `main()` выполненной работы.

### Этапы тестирования

1. На соответствие обязательным требованиям (частично):

    **Content**:
    * проверка некоторых пунктов CG (длина строк, пробелы, окончания строк/файла)
    * проверка на порядок сдачи работ (см. файл .config в корне репозитория)
	
    **Branch**:
    * проверка, что лабораторная отправлена из форка
    * проверка, что существует только один начальный коммит

    **Author**:
    * проверка, что не затронуты чужие работы
    * проверка, что не затронуты файлы в корне репозитория
    * проверка, что имя папки в нижнем регистре

2. На сборку (с помощью Makefile)

    **Build**: вызывается команда `make build-ivanov.ivan/T0`
   
3. Приёмочные тесты:

    **Acceptance**: зависят от лабораторной работы. Для не пройденных тестов показываются входные данные и ожидаемый вывод
	
### Сборка с помощью Makefile

Все работы автоматически обнаруживаются и могут быть построены с использованием нескольких целей.

Все исходные тексты в каждой работе идентифицируются по расширению ".cpp".

Идентификатором каждой работы является строка `lastname.firstname/labnumber`, которая в дальнейшем именуется `labid`.

Makefile автоматически строит программу для каждой работы.
Так как имя программы в общем случае неизвестно, специальная цель выполняет запуск построенной программы с передачей параметров.

Поддерживаемые цели:

* `build-labid`: построение лабораторной работы, например

        $ make build-ivanov.ivan/T2

* `run-labid`: запуск построенной программы, например

        $ make run-ivanov.ivan/T2

    Для передачи дополнительных параметров используется переменная
    `ARGS` (при помощи GNU Make):

        $ make run-ivanov.ivan/T1 ARGS="1 ascending"

    или (c использованием Bourne Shell):

        $ ARGS="1 ascending" make run-ivanov.ivan/T1

    или (Bourne Shell, с сохранением в окружении процесса):

        $ export ARGS="1 ascending"
        $ make run-ivanov.ivan/T1

* `labs`: список всех лабораторных в проекте.

Дополнительной возможностью является запуск динамического анализатора [Valgrind](http://valgrind.org) для запускаемых программ.
Для этого необходимо указать в переменной `VALGRIND` параметры анализатора так, как это делается для `ARGS`.
