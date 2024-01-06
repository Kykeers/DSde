# Домашнее задание #3
# СОЗДАЁМ ЛОКАЛЬНЫЙ РЕПОЗИТОРИЙ
1. создаем папку на рабочем столе
2. Заходим в приложение Visual Studio code
3. вызываем терминал и прописываем git init
* git init - *Команда git init используется для инициализации нового репозитория Git в текущем каталоге. Когда вы выполняете эту команду в пустой папке или в проекте, Git создает скрытую подпапку .git, которая содержит все необходимые файлы для работы с репозиторием.*
4. создаем файл с расшырением md это нужно чтобы он отображался в Markdown, с помощью команды git add <имя файла>  добовляем его в репозиторий затем вводим команду git commit -m"message" для того чтобы его закоментировать
* Команда git add используется для добавления изменений в индекс (также известный как "staging area"). Индекс представляет собой промежуточный этап перед фиксацией изменений с помощью команды git commit.
* Команда git commit -m используется для создания нового коммита (фиксации) в репозитории Git с сообщением о коммите в командной строке. Это позволяет вам описать суть внесенных изменений.
5. Каждый раз после того как мы добавили какие-то изменения в наш файл нам  нужно его сохранять, добавлять в репозитории и cделать  для него commit.
* Команда git status используется для вывода информации о текущем состоянии вашего рабочего каталога и репозитория Git. Эта команда показывает, какие файлы были изменены, добавлены в индекс или исключены, и в каком состоянии они находятся.


# ПЕРЕМЕЩАЕМСЯ МЕЖДУ КОМИТАМИ
* **_Команда git log_** используется для просмотра истории коммитов в репозитории Git. Когда вы выполните эту команду, Git выведет список коммитов, начиная с самого нового и заканчивая самым старым. Информация о каждом коммите включает в себя автора, дату, уникальный идентификатор коммита (хеш), и сообщение коммита.
* **_Команда git checkout_** в Git используется для переключения между ветками или восстановления файлов из репозитория.( А также для перемещения между комитами) 
1. После ввода команды git log выводится список коммитов, у каждого кометы есть уникальный идентификатор чтобы перемещаться между кометами нам понадобится идентификатор, достаточно скопировать первые четыре символа.
2. затем вводим команду git checkout и вставляем скопированный идентификатор
3. чтобы вернуться в актуальное состояние файла нам нужно ввести команду git checkout master или main. мы вернёмся к последнему сохранению.


# СОЗДАНИЕ НОВЫХ ВЕТОК
* **_Команда git branch_** в Git используется для просмотра, создания и удаления веток в репозитории
* **_команда git branch <название_новой_ветки>_** используется для создания новой ветки
* **_команда git checkout <название_ветки>_** используется для  перемещения между ветками
 **_git checkout -b <новая_ветка>_** Эта команда создает новую ветку и сразу переключает вас на нее.
 * **_git branch -d <название_ветки>_** Эта команда удаляет указанную ветку. Если ветка слита с другой веткой, В противном случае она её не удалит
 * **_git branch -D <название_ветки>_** Эта команда удаляет указанную ветку даже в том случае если ветка не была слита с другой веткой.
 * **_git merge <исходная_ветка>_** Эта команда выполняет слияние двух веток.
1. Вводим команду git branch <название_новой_ветки>( если название ветки состоит из двух или более слов не забываем прописывать нижние чёрточки)
2. Вводим команду git branch, появляется список веток.В этом списке можно увидеть на какой ветке мы находимся.
3. Вводим команду git checkout <название_ветки> чтобы переходить с одной ветки на другую.
4. После перехода на побочную ветку и выполнение в ней каких-либо изменений можно выполнить слияние двух веток. Для этого нам нужно в этой ветке сохранить изменения, добавить их в репозиторию и сделать комит,вернуться в ветку в которую мы хотим выполнить слияние затем задать команду git merge<исходная_ветка>. Слияние двух веток может происходить как с конфликтами так и без конфликтов, слияние двух веток с конфликтами происходит в том случае если в обоих ветках на одних и тех же сроках есть какие-либо записи.
5. После слияния веток и решения конфликтов если они присутствовали можно удалить побочную ветку для этого надо ввести команду git branch -d <название_ветки>.
# СОЗДАНИЕ УДАЛЁННОГО РЕПОЗИТОРИЯ
Для создания удалённого репозитория нам понадобится GitHab это сайт на котором хранится проекты других пользователей ,также мы можем добавлять туда свои проекты. Это нужно для того чтобы выполнять командные работы.
 на сайте мы создаем  новый удалённый репозитории а затем мы его должны  п привязать его к локальному репозиторию
 Нам будут предоставлены три варианта 
 1. создайте новый репозиторий в командной строкe
 2. отправить существующий репозиторий из командной строки
 3. импортируйте код из другого репозитория 

 ## выполним первый вариант
* на рабочем столе создае папку
* Заходим в приложени Visual Studio code
* Создаем файл README с расширением md  сохраняем его, добавляем в репозиторий и делаем commit.
* В терминале прописываем следующие команды
1. git init
2. git add README.md
3. git commit -m "first commit"
4. git branch -M main
5. git add origin https://github.com/fuad1229/fuad.git
6. git push -u origin main

* После выполнения каких-либо изменений сохраняем их, добавляем В репозиторий и делаем комми. Чтобы связать локальный репозитории с удалённым репозитории прописываем команду git push.
* также мы можем выполнить изменения в удалённом репозитории и связать его с локальным. Для этого в githab мы заходим на файл который мы создали нажимаем на иконку с карандашом  прописываем изменения затем нажимаем на вкладку **commit changes** и прописываем комит.Затем перехордим в Visual Studio code и в терминале прописываем команду git pull

# РАБОТА В ЧУЖОМ РЕПОЗИТОРИИ

* Для того чтобы работать в чужом репозитории нам нужно найти нужный нам репозитории затем в вкладки **code** скопировать репозиторий и создать клон, в этом случае мы не будем иметь никакой связи мы сможем работать только в локальном репозитории без изменений в удалённом
* Для того чтобы была связь с удалённом репозитории мы должны выбрать вкладку **Fork** в появившимся окне нужно прописать название и нажать на кнопку *Creating Fork* после того как страница загрузится, опять нажимаем на кнопку **code** и копируем ссылку.
* Затем на рабочем столе создаем новую папку заходим в приложение Visual Studio code открываем эту папку и в терминале прописываем следующий код **git clone** и добовляем ссылку удаленного репозитория.
* После того как мы пропишем эту команду у нас появится ещё один репозиторий для того чтобы перейти на него мы должны ввести следующую команду **cd название папки**
* теперь когда мы находимся в нужном нам репозитории мы создаем побочную ветку **git branch название_ветки** и переходим на неё **git checkout название_ветки**
