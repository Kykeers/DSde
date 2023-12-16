# Домашнее задание #3
### Как задать имя пользователя и адрес электронной почты
*git config --global user.name "user_name"*

*git config --global user.email "user_email"*

### Инициализация репозитория
*git init*

### Добавление файлов
*git add file_name.md* - добавление файла в область подготовленных файлов

### Внесение изменений
*git commit -m "message"* 

### Просмотр истории коммитов с изменениями
*git log -p* 

### Просмотр заданного коммита
*git show <хеш коммита>* 

### Просмотр изменений до коммита
*git diff*

### Изменение последнего коммита
git commit --amend -m "message"

### Создание новой ветки
*git branch new_branch_name*

### Переход на другую ветку
*git checkout branch_name*

### Удаление локальной копии ветки
*git branch -d branch_name*

### Слияние двух веток
*git merge branch_name*

### Добавление удаленного репозитория
*git remote add <short_name и url>*

### Получение дополнительных сведений об удаленном репозитории
*git remote show*

### Отправка изменений в удаленный репозиторий
*git push origin main*

### Получение изменений из удаленного репозитория
*git pull*

### Отправка новой ветки в удаленный репозиторий
*git push -u origin new_branch*

