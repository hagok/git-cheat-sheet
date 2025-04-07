# Git console шпаргалка

Здесь собраны самые важные git-команды, как для новичка так и для продвинутого git-владельца. 
_(А если честно, то просто писал для себя, чтобы не юзать гугл и не тупить)_



## Оглавление

0. [git init](#git-init)
1. [git clone](#git-clone)
2. [git add](#git-add)
3. [git commit](#git-commit)



## 







#### git init
`git init` используется для инициализации нового репозитория Git в указанном каталоге.
<br />


#### git clone
`git clone <ссылка на репозиторий>` создаёт копию публичного существующего репозитория. Она позволяет скачать все файлы и историю изменений из удалённого репозитория на локальный компьютер.
<br />
`git clone https://<Ваш токен>@github.com/hagok/example-repository.git` создаёт копию закрытого репозитория из github. Токен можно получить в личном кабинете github -> Develop settings.
<br />

#### git add
`git add` добавляет изменения в промежуточная область (индекс), где можно подготовить изменения перед их фиксацией в репозитории.
<br />
`git add file_name.html` добавляет в индекс один файл.
<br />
`git add file_name_1.html file_name_2.txt file_name_3.lol` добавляет в индекс несколько файлов.
<br />
`git add . ` добавляет в индекс все изменённые файлы.
<br />

#### git commit
`git commit` фиксирует изменения в репозитории.
<br />
`git commit -m <Ваш комментарий по изменениям>`
<br />