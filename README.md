# custom-cpp-builder
свой сборщик проектов на c++ для проектов без хитростей

# сборка
создайте файл `FLAGS` в корневой папке проекта
в нём запишите флаги, необходимые для компилятора/линковщика (используется только g++), например:
```
sorce_code.cpp -flag0 -flag1 -flag2
```
`-c` и `-o obj_name` указывать не надо.
также, если нужно указать флаги для итогового исполняемого файла или всех файлов сразу, то используйте вместо имени файла ключевые слова `result` и `all` соответственно

# результат
Папка `build` - папка с исполняемым файлом и `tmp` с объектами.

# критерии файлов
все `#include` должны быть указаны в начале файла и **не должно быть** рекурсии заголовочных файлов. директивы `#pragma`, `#include` и пустые строки игнорируются. Библиотечные заголовники должны добавляться только с треугольными скобками.

