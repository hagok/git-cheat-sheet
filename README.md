# Git console шпаргалка

Здесь собраны самые важные git-команды, как для новичка так и для продвинутого git-владельца. 
_(А если честно, то просто писал для себя, чтобы не юзать интернеты и не тупить)_

 
## 🔄 Работа с репозиторием
`git init` – [Инициализируем репозиторий](#git-init) <br/>
`git clone` – [Копируем репозиторий](#git-init) <br/>
`git add` – [Добавляем изменения](#git-init) <br/>
`git commit` – [Фиксируем изменения](#git-init) <br/>
`git status` – [Проверяем статус](#git-init) <br/>
`git log` – [Смотрим историю коммитов](#git-init) <br/>
`git show` – [Просмотр конкретного коммита](#git-init) <br/>
`git diff` – [Смотрим изменения до коммита](#git-init) <br/>
`git rm` – [Удаляем файлы](#git-init) <br/>
`git mv` – [Перемещаем/переименовываем файлы](#git-init) <br/>

## 🌿 Ветки (Branches)
`git branch` – [Работа с ветками](#git-init) <br/>
`git checkout` – [Переключение между ветками](#git-init) <br/>
`git merge` – [Слияние веток](#git-init) <br/>
`git rebase` – [Перебазирование](#git-init) <br/>

## ☁ Удалённые репозитории (Remote)
`git remote` – [Управление удалёнными репозиториями](#git-init) <br/>
`git push` – [Отправка изменений на сервер](#git-init) <br/>
`git pull` – [Загрузка изменений с сервера](#git-init) <br/>
`git fetch` – [Получение изменений без слияния](#git-init) <br/>

## ⏪ Отмена изменений
`git reset` – [Отмена коммитов](#git-init) <br/>
`git revert` – [Создание отменяющего коммита](#git-init) <br/>
`git stash` – [Временное сохранение изменений](#git-init) <br/>

## 🏷 Теги (Tags)
`git tag` – [Работа с тегами версий](#git-init) <br/>

## ⚙ Конфигурация
`git config` – [Настройка Git](#git-init) <br/>
 
#
 
<br/><br/>
## 📝 Подробное описание команд


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
<br /><br />













