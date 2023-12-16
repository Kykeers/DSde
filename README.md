# Домашнее задание #3
***Мамедов Шамиль***
# **Что такое Git **
`Git` — *самая популярная в мире система контроля версий (от англ. Version Control System, VCS). Неудивительно, что навык работы с Git стал обязательным для программистов*.
`Git` — *это бесплатная распределенная система контроля версий с открытым исходным кодом, которая обрабатывает изменения кода в программных проектах любого размера. Git позволяет нескольким разработчикам одновременно работать над одним проектом*.
# Установка
Итак, мы установили git, теперь нужно добавить немного настроек. Есть довольно много опций, с которыми можно играть, но мы настроим самые важные: наше имя пользователя и адрес электронной почты. Откройте терминал и запустите команды:

git config --global user.name "My Name"
git config --global user.email myEmail@example.com
# Создание локального репозитория `Git`
***
Откройте терминал (консоль, Git Bash, командную строку) и перейдите в каталог, в котором на компьютере будет храниться проект.

Например.
  ```  
cd ~/Desktop

mkdir myproject

cd myproject/
```
Создайте репозиторий в выбранной папке, выполнив команду `git` init:

**git init [имя репозитория]**

# Команды
`git` add Переносит изменения из рабочего каталога в раздел проиндексированных файлов

`git` status Показывает состояние рабочего каталога и проиндексированного снимка состояния

`git` commit Получает проиндексированный снимок состояния и выполняет его коммит в историю проектa

`git` branch Эта команда выступает универсальным инструментом администрирования веток

`git` checkout С командой git checkout можно не только получать старые коммиты и прежние версии файлов, но и осуществлять навигацию по существующим веткам

`git `merge  Эффективный способ интеграции изменений из разошедшихся веток

`git `log   Позволяет изучить предыдущие версии проекта

`git pull Команда git pull — это автоматизированная версия команды git fetch. Она загружает ветку из удаленного репозитория и сразу же объединяет ее с текущей веткой

`git` push Команда git push противоположна команде извлечения (с некоторыми оговорками). С ее помощью можно перенести локальную ветку в другой репозиторий

`git` remote  для администрирования удаленных подключений. 

`git` clone Создает копию существующего репозитория Git

`git` init Инициализирует новый репозиторий Git

`git` revert  Отменяет коммит снимка состояния. Если вы обнаружили ошибочный коммит, его можно легко и безопасно удалить из базы кода с помощью команды git revert.

`git `remote add для добавления или подключения к удаленному репозиторию.

`git` remote -v для просмотра подключенных удаленных репозиториев

 `git` push -u origin создаёт в удалённом репозитории ветку, соответствующую локальной и связывает их.

***
# Создание  удаленного репозитория `GitHub`
**GitHub** позволяет отслеживать код, когда вы работаете с командой и требуется внести модификации. Чтобы создать новый репозиторий, выполните следующие действия:

Войдите в систему и перейдите на домашнюю страницу **GitHub**.

Найдите опцию New repository под знаком плюса рядом с фотографией профиля в правом верхнем углу.



# Добавление файлов в удаленный репозиторий


   `git remote add origin https://github.com/[ваш логин]/[название репозитория.git]`

   `git push -u origin maste`
