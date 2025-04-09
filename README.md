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
git status                   # полный статус  
git status -s                # краткий вывод  
git status <ид. репозитория> # просмотр статуса конкретного репозитория 
```
<br />

### git log
`git log` – история коммитов.
```
git log              # полная история  
git log -p           # изменения, внесённые в каждый файл
git log --oneline    # сокращённый вид  
git log --graph      # с визуализацией веток  
```
_(выход — клавиша q)_
<br /><br />

### git show
`git show <хэш>` – показывает изменения в конкретном коммите.
```
git show 0af17e73721dbe0c40011b82ed4bb1a7dbe3ce29
git show 0af17e7  
```
_(выход — клавиша q)_
<br /><br />

### git diff
`git diff` – сравнение изменений.
```
git diff             # изменения в рабочей директории  
git diff --staged    # изменения в индексе 
git diff file.html   # можно указать имя файла как параметр и просмотреть изменения, внесённые только в этот файл.
```
_(выход — клавиша q)_
<br /><br />

#### git rm
`git rm` – удаление файлов.
```
git rm file.txt         # удалить файл из Git 
git rm dir/file.html    # удаляем файлы из текущего рабочего дерева. При этом файлы удаляются и из индекса
git rm dir/*.html       # можно использовать маски файлов (например *.html) для удаления всех файлов, соответствующих критерию
```
<br />

#### git mv
`git mv` – переименовывание и перемещение файлов.
```
git mv old.txt new.txt      # переименовать файл
git mv dir1/file.html dir2  # перемещение файлов из одной папки в другую
```
<br />


  
### git branch
`git branch` - работа с ветками
```
git branch                  # список веток  
git branch new-feature      # создать новую ветку  
git branch -d old-branch    # удалить ветку  
```
<br />

### git checkout 
`git checkout` - переключение между ветками
```
git checkout main           # переключиться на main 
git checkout -b new-branch  # создать и переключиться
git switch main             # переключиться на main, switch это новое прочтение checkout
```
<br />

### git merge 
`git merge` - слияние: сохраняет историю в виде дерева, подходит для публичных веток (main, develop)
```
git merge feature       # влить ветку feature в текущую 
git merge --abort       # отмена слияния из-за конфликтов

```
<br />

### git rebase 
`git rebase` - перебазирование: перестраивает историю, делая её линейной, лучше для локальных веток перед слиянием
```
git rebase main         # перебазировать текущую ветку на main 
```
<br />

### git remote
`git remote` - управление удалёнными репозиториями
```
git remote                                              # просмотр списка удалённых репозиториев
git remote -v                                           # показывает краткий список имён удалённых репозиториев
git remote add origin https://github.com/user/repo.git  # добавление нового удалённого репозитория
git remote show <имя>                                   # просмотр информации об удалённом репозитории
git remote rename <старое-имя> <новое-имя>              # переименование удалённого репозитория
git remote remove <имя>                                 # удаление удалённого репозитория
```
<br />

### git push
`git push` - команда для отправки локальных изменений в удалённый репозиторий
```
git push                             # отправить изменения
git push origin main                 # явное указание репозитория и ветки
git push origin feature:new-feature  # отправка в ветку с другим именем
git push --all origin                # отправка всех локальных веток
git push origin --delete old-branch  # удаление удалённой ветки
```
<br />

### git pull
`git pull` - команда для получения изменений из удалённого репозитория и их автоматического слияния с локальной веткой
```
git pull                            # получить изменения с сервера  
git pull origin main                # явное указание репозитория и ветки
git pull --rebase origin main       # использование rebase вместо merge
git pull --no-commit origin feature # получение изменений без автоматического коммита
git pull --ff-only origin main      # безопасное обновление (только fast-forward)
```
<br />

### git fetch
`git fetch` - команда для загрузки изменений из удалённого репозитория без автоматического слияния с локальными ветками
```
git fetch             # получение всех изменений из origin
git fetch origin      # явное указание репозитория и ветки
git fetch origin main # получение конкретной ветки
git fetch --all       # получение всех удалённых репозиториев
git fetch --prune     # получение изменений с очисткой устаревших веток
``` 
<br />






### git reset
`git reset` - 
```
git reset --soft HEAD~1  # отменить коммит, сохранив изменения  



```
<br />





### git revert
`git revert` - 
```
git revert a1b2c3d       # создать отменяющий коммит  


```
<br />




### git stash
`git stash` - 
```
git stash          # спрятать изменения  
git stash pop      # вернуть изменения  
```
<br />





















### git tag
`git tag` Работа с тегами:
```
git tag v1.0          # создать лёгкий тег  
git tag -a v1.0 -m "Версия 1.0"  # аннотированный тег  
```
<br />










### git config
`git config` Настройка Git:
```

git config --global user.name "Имя"  
git config --global user.email "email@example.com"  
git config --global core.editor "code --wait"  # VS Code как редактор 
``` 
<br />








###💡 Совет:

```
git alias --global lol "log --oneline --graph"  
```
Теперь можно писать git lol для красивого вывода истории!

Если что-то забыл — просто загляни в эту шпаргалку! 😉

<br/>
[Пошли наверх](#git-console-шпаргалка) <br/>
