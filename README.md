# Отчёт по ДЗ №13.
## Старцев Евгений Борисович, БПИ219.
### Инструкция по компиляции и запуску:
Скомпилируйте файл rec_checker.c с помощью компилятора gcc:

```
gcc -o rec_checker rec_checker.c
```

Запустите программу:

```
./rec_checker
```

Программа выведет глубину рекурсии для символьных связей в вашей системе и создаст файлы в директории test_files.

### Описание программы:
Программа написана на языке C и предназначена для определения глубины рекурсии символьных связей при открытии файлов в Unix-подобных операционных системах.

Сначала программа создает директорию test_files, после чего создает базовый файл a в этой директории. Затем программа начинает создавать символьные связи на этот файл, каждый раз создавая новую связь на последний созданный файл, и пытаясь открыть новый файл через связь. Этот процесс повторяется, пока открыть файл через связь не станет невозможно. Это означает, что была достигнута максимальная глубина рекурсии для символьных связей. Программа затем выводит эту глубину на экран.

Программа также содержит проверки на ошибки после каждого системного вызова, чтобы обеспечить корректное выполнение и предоставить подробную информацию об ошибках, если они происходят.

Важно отметить, что максимальная глубина рекурсии в этой программе задается константой MAX_RECURSION_DEPTH, которая равна 1000. В зависимости от вашей системы, вам может потребоваться увеличить или уменьшить это значение.