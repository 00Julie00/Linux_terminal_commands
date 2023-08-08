
## Примеры использования основных команд Linux:

1. Посмотреть где я - `pwd`
2. Создать папку - `mkdir qa_course`
3. Зайти в папку - `cd qa_course`
4. Создать 3 папки - `mkdir one two three`
5. Зайти в любоую папку - `cd one`
6. Создать 5 файлов (3 txt, 2 json) - `touch file1.txt file2.txt file3.txt test1.json test2.json`
7. Создать 3 папки - ` mkdir first second third`
8. Вывести список содержимого папки - `ls -la`
9. Открыть любой txt файл - `cat file1.txt` 
10. Написать туда что-нибудь, любой текст - `cat > file1.txt`
11. Cохранить и выйти - Ctrl+C 
12. Выйти из папки на уровень выше - `cd ..`
13. Переместить любые 2 файла, которые вы создали, в любую другую папку - `mv one/file1.txt one/test2.json two`
14. Cкопировать любые 2 файла, которые вы создали, в любую другую папку - `cp one/file3.txt one/test1.json three`
15. Найти файл по имени - `find . -name "file*"`
16. Просмотреть содержимое в реальном времени - `tail -f file3.txt | grep "авто*"`
17. Вывести несколько первых строк из текстового файла - `head file3.txt`
18. Вывести несколько последних строк из текстового файла - `tail -f file3.txt`
19. Просмотреть содержимое длинного файла - `less file3.txt`
    Для выхода из less и возврата к командной строке нажать `q`
20. Вывести дату и время - `date`
    
## Задание со *
### Часть 1
Задача:
1. Отправить http запрос на сервер http://162.55.220.72:5006/terminal-hw-request
2. Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)

Решение:
1. curl -v -s -X GET  http://162.55.220.72:5006/terminal-hw-request
2. curl "http://162.55.220.72:5005/get_method?name=(Julia)&age=(39)"
   
### Часть 2
Задача:
Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

Решение:
1. Создадим файл для скритпа с расширением `sh` - `touch script.sh`
2. Сделаем файл скрипта исполняемым - `chmod +x script.sh`
3. Откроем файл через редактор vim для написания команд скрипта - `vim touch script.sh`
4. Внесем в файл:
   
`#!/bin/bash`

`cd qa_course`

`echo "cd qa_course"`

`mkdir four five six`

`echo "mkdir four five six"`

`cd five`

`echo "cd five"`

`touch file4.txt file5.txt file6.txt test3.json test4.json`

`echo "touch file4.txt file5.txt file6.txt test3.json test4.json"`

`mkdir d1 d2 d3`

`echo "mkdir d1 d2 d3"`

`ls -la`

`echo "ls -la"`

`mv file4.txt test3.json d1`


`echo "mv file4.txt test3.json d1"`

Для того чтобы мы могли следить за ходом выполнения каждой команды, выводим на экран текст команды с помощью команды `echo` 

5. Выходим из редактора с помощью следующих действий:
   
 `Esc`

 `:wq`
 
 `Enter`
 1. Запускаем наш скрипт - `bash script.sh` 
    При необходимости прописываем путь где лежит файл со скриптом.
