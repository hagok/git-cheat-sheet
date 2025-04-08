# Git console шпаргалка

Здесь собраны самые важные git-команды, как для новичка так и для продвинутого git-владельца. 
_(А если честно, то просто писал для себя, чтобы не юзать гугл и не тупить)_



## Работа с репозиторием
0. git init - [Инициализируем репозиторий](#git-init)
1. git clone - [Копируем репозиторий](#git-clone)
2. git add - [Добавляем изменения](#git-add)
3. git commit - [Вносим изменения](#git-commit)
4. git status - [Проверяем статус репозитория](#git-status)
5. git log - [Смотрим логи коммитов с изменениями](#git-log)
6. git show - [Смотрим определённый коммит](#git-show)
7. git diff - [Смотрим изменения до коммита](#git-diff)
8. git rm - [Удаляем файлы из текущего дерева](#git-rm)
9. git mv - [Перемещаем файлы](#git-mv)


##


## Конфигурации
0. [Задаём имя пользователя](#задаём-имя-пользователя)
1. [Задаём адрес электронной почты](#задаём-адрес-электронной-почты)
2. [Кэшируем учётные данные](#кэшируем-учётные-данные)
##

 







#### git init
`git init` используется для инициализации нового репозитория Git в указанном каталоге. При инициализации он создаст скрытую папку. В ней содержатся все объекты и ссылки, которые Git использует и создаёт в истории работы над проектом.
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


#### git status
`git status` просмотр статусов всех репозиториев, действие распространяется на подготовленные, неподготовленные и неотслеживаемые файлы.
<br />
`git status <идентификатор репозитория>` просмотр статуса конкретного репозитория 
<br />


#### git log
`git log` просмотр изменений, внесённые в репозиторий. Он отображает список последних коммитов в порядке выполнения.
<br />
`git log -p` добавив флаг -p, вы можете подробно изучить изменения, внесённые в каждый файл.
<br />
`q` выход из логов.
<br />


#### git show
`git show 0af17e73721dbe0c40011b82ed4bb1a7dbe3ce29` просмотр полного списка изменений, внесённых конкретным коммитом, с указанием идентификатора или хеш коммита. Значение хеша уникально для каждого коммита, созданного в вашем репозитории.
<br />
`git show 0af17e` можно использовать сокращённый хеш.
<br />
`q` выход из просмотра.
<br />


#### git diff
`git diff` просмотр списка изменений, внесённых в репозиторий. По умолчанию отображаются только изменения, не подготовленные для фиксации.
<br />
`git diff --staged` просмотр подготовленных изменени.
<br />
`git diff file.html` можно указать имя файла как параметр и просмотреть изменения, внесённые только в этот файл.
<br />
`q` выход из просмотра.
<br />


#### git rm
`git rm dir/file.html` удаляем файлы из текущего рабочего дерева. При этом файлы удаляются и из индекса.
<br />
`git rm dirname/*.html` можно использовать маски файлов (например *.html) для удаления всех файлов, соответствующих критерию.
<br />


#### git mv
`git mv dir1/file.html dir2` перемещение файлов из одной папки в другую. Для него указывается источник source и назначение destination. Источник — реально существующий файл или папка, а назначение — существующая папка. При выполнении команды файл или папка, указанные как источник, будут перемещены в папку назначения. Индекс будет обновлён соответственно, но изменения нужно записать.
<br />












 

















<br /><br /><br />

#### Задаём имя пользователя
`git config --global user.name "Tara Routray"` Новое имя будет автоматически отображаться в последующих коммитах, отправленных на GitHub через командную строку.
<br />

#### Задаём адрес электронной почты
`git config --global user.email "dev@tararoutray.com"` Новый адрес электронной почты будет автоматически отображаться во всех дальнейших коммитах, поданных на GitHub через командную строку.
<br />

#### Кэшируем учётные данные
`git config --global credential.helper cache` Кэшировать учётные данные можно с помощью параметра config с флагом --global. Так вы избавитесь от необходимости вручную вводить имя пользователя и пароль при создании нового коммита.
<br />



