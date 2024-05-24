### Условие

Скрипт на bash, который на вход принимает два параметра - две директории (входная директория и выходная директория). Во входной директории могут находиться как файлы, так и вложенные директории (внутри которых тоже могут быть как файлы, так и папки) - уровень вложенности может быть любой. 

Задача скрипта - "обойти" входную директорию и скопировать все файлы из нее (и из всех сложенных директорий) в выходную директорию - но уже без иерархии, а просто все файлы - внутри выходной директории.

В разных поддиректориях входной директории могут быть файлы с одинаковым названием. В момент копирования в выходную аудиторию необходимо такие ситуации  разрешить без потери файлов и содержания файлов.

### Как решается проблема с поиском скрытых файлов или тех, к которым нужно право доступа?

Поиск скрытых файлов, осуществляется с помощью комманды find

```
$ find . -name ".*" -type f
```

Файлы, к которым нужно предоставить право доступа, считываются с помощью команды chmod

```
chmod 777 $input
```
