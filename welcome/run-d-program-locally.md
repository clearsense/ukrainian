# Локальний запуск програм D

У стандартній комплектації є компілятор D `dmd`, скрипто-подібний
інструмент `rdmd` для запуску додатку *на льоту* та пакетний менеджер `dub`.

### Компілятор DMD

Компілятор *DMD* компілює D файл(и) та створює виконуваний файл.
У терміналі компілятор *DMD* можна викликати разом з іменем файлу:

    dmd hello.d

Існує багато опцій, які надають можливість змінювати стандартну поведінку
компілятора *DMD*.
Вивчіть [онлайн документацію](https://dlang.org/dmd.html#switches) чи
виконайте у терміналі `dmd --help`, щоб подивитися список доступних параметрів.

### Компіляція «на льоту» за допомогою `rdmd`

Разом з компілятором DMD постачається допоміжний інструмент `rdmd`, який
стежить за тим, щоб скомпілювати всі залежності і автоматично запустити
отриману програму:

    rdmd hello.d

На UNIX системах можна розмістити `#!/usr/bin/env rdmd` у перший
рядок D файлу, який потрібно виконувати, щоб дозволити скрипто-подібне
використання.

Вивчіть [онлайн документацію](https://dlang.org/rdmd.html) чи виконайте
у терміналі `rdmd --help`, щоб подивитися список доступних параметрів.

### Пакетний менеджер `dub`

У світі D стандартним пакетним менеджером є [`dub`](http://code.dlang.org).
Якщо `dub` встановлено локально, новий проект `hello` можна створити,
виконавши наступну коману у терміналі:

    dub init hello

Команда `dub` всередині цієї теки завантажить всі залежності, скомпілює
проект і запустить його.
Команда `dub build` лише скомпілює проект.

Вивчіть [онлайн документацію](https://code.dlang.org/docs/commandline)
чи виконайте у терміналі `dub help` щоб переглянути доступні команди і особливості.

Всі доступні dub-пакети можна переглянути через [веб-інтерфейс](https://code.dlang.org).