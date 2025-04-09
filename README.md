# Git console шпаргалка

Здесь собраны самые важные git-команды, как для новичка так и для продвинутого git-владельца. 
_(А если честно, то просто писал для себя, чтобы не юзать интернеты и не тупить)_

 
## 🔄 Работа с репозиторием
`git init` – [Инициализируем репозиторий](#git-init) <br/>
`git clone` – [Копируем репозиторий](#git-clone) <br/>
`git add` – [Добавляем изменения](#git-add) <br/>
`git commit` – [Фиксируем изменения](#git-commit) <br/>
`git status` – [Проверяем статус](#git-status) <br/>
`git log` – [Смотрим историю коммитов](#git-log) <br/>
`git show` – [Просмотр конкретного коммита](#git-show) <br/>
`git diff` – [Смотрим изменения до коммита](#git-diff) <br/>
`git rm` – [Удаляем файлы](#git-rm) <br/>
`git mv` – [Перемещаем/переименовываем файлы](#git-mv) <br/>

## 🌿 Ветки (Branches)
`git branch` – [Работа с ветками](#git-branch) <br/>
`git checkout` – [Переключение между ветками](#git-checkout) <br/>
`git merge` – [Слияние веток](#git-merge) <br/>
`git rebase` – [Перебазирование](#git-rebase) <br/>

## ☁ Удалённые репозитории (Remote)
`git remote` – [Управление удалёнными репозиториями](#git-remote) <br/>
`git push` – [Отправка изменений на сервер](#git-push) <br/>
`git pull` – [Загрузка изменений с сервера](#git-pull) <br/>
`git fetch` – [Получение изменений без слияния](#git-fetch) <br/>

## ⏪ Отмена изменений
`git reset` – [Отмена коммитов](#git-reset) <br/>
`git revert` – [Создание отменяющего коммита](#git-revert) <br/>
`git stash` – [Временное сохранение изменений](#git-stash) <br/>

## 🏷 Теги (Tags)
`git tag` – [Работа с тегами версий](#git-tag) <br/>

## ⚙ Конфигурация
`git config` – [Настройка Git](#git-config) <br/>
 
#
 
<br/><br/>
## 📝 Подробное описание команд
<br/>

### git init
`git init` – создаёт новый локальный репозиторий в текущей папке (появится скрытая папка .git).
```
git init
```
<br />

### git clone
`git clone <URL>` – клонирует удалённый репозиторий на компьютер.
```
git clone https://github.com/user/repo.git  
git clone git@github.com:user/repo.git  # через SSH 
```
Для приватных репозиториев:
```
git clone https://<ТОКЕН>@github.com/user/repo.git  
```
<br />

### git add
`git add` – добавляет изменения в индекс (подготовка к коммиту).
```
git add file.txt         # добавить конкретный файл  
git add .                # добавить все изменения  
git add *.js             # добавить все JS-файлы 
```
<br />

### git commit
`git commit` – фиксирует изменения в репозитории.
```
git commit -m "Сообщение"  # стандартный коммит  
git commit --amend         # изменить последний коммит  
```
<br />

### git status
`git status` – показывает состояние изменённых/добавленных/удалённых файлов.
```
git status       # полный статус  
git status -s    # краткий вывод  
git status <ид. репозитория> # просмотр статуса конкретного репозитория 
```
<br />

### git log
`git log` – история коммитов.
```
git log              # полная история  
git log -p    # изменения, внесённые в каждый файл
git log --oneline    # сокращённый вид  
git log --graph      # с визуализацией веток  
```
(выход — клавиша q)
<br />

### git show
`git show <хэш>` – показывает изменения в конкретном коммите.
```
git show 0af17e73721dbe0c40011b82ed4bb1a7dbe3ce29
git show 0af17e7  
```
(выход — клавиша q)
<br />

### git diff
`git diff` – сравнение изменений.
```
git diff             # изменения в рабочей директории  
git diff --staged    # изменения в индексе 
git diff file.html	 # можно указать имя файла как параметр и просмотреть изменения, внесённые только в этот файл.
```
(выход — клавиша q)
<br />




















 
### git rm / git mv
Удаление и перемещение файлов:

git rm file.txt      # удалить файл из Git  
git mv old.txt new.txt  # переименовать файл
<br />







  
### git branch
Работа с ветками:

git branch                  # список веток  
git branch new-feature      # создать новую ветку  
git branch -d old-branch    # удалить ветку  
<br />










### git checkout / git switch
Переключение между ветками:

git checkout main           # переключиться на main  
git checkout -b new-branch  # создать и переключиться
<br />









  
### git merge / git rebase
Слияние и перебазирование:

git merge feature       # влить ветку feature в текущую  
git rebase main         # перебазировать текущую ветку на main 
<br />







 
### git push / git pull
Работа с удалённым репозиторием:

git push origin main    # отправить изменения  
git pull               # получить изменения с сервера  
<br />








### git reset / git revert
Отмена изменений:

git reset --soft HEAD~1  # отменить коммит, сохранив изменения  
git revert a1b2c3d       # создать отменяющий коммит  
<br />








### git stash
Временное сохранение изменений:

git stash          # спрятать изменения  
git stash pop      # вернуть изменения  
<br />








### git tag
Работа с тегами:

git tag v1.0          # создать лёгкий тег  
git tag -a v1.0 -m "Версия 1.0"  # аннотированный тег  
<br />










### git config
Настройка Git:

git config --global user.name "Имя"  
git config --global user.email "email@example.com"  
git config --global core.editor "code --wait"  # VS Code как редактор  
<br />








💡 Совет:


git alias --global lol "log --oneline --graph"  
Теперь можно писать git lol для красивого вывода истории!

Если что-то забыл — просто загляни в эту шпаргалку! 😉