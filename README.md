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
git status       			 # полный статус  
git status -s    			 # краткий вывод  
git status <ИД. РЕПОЗИТОРИЯ> # просмотр статуса конкретного репозитория 
```
<br />

