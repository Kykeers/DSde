# Домашнее задание #3
## 4 Шага работы с котролем версий :
1. Внести изменения;
2. Сохранить изменения (CTRL+S);
3. Добавить файл с изменениями; 
4. Зафиксировать эти изменения;

## Коротко об оформлени в Markdown.

### Выделение текста:

*Курсив* - обромление звездочками (*) выделяют текст курсивом, так же можно использовать обромление нижними подчеркиваниями ( _ ).

**Полужирный шрифт** - обромление двумя звездочками (**) выделяют текст полужирным, так как в случая с курисовом можно использовать нижние подчеркивания но в этом случае двойные ( _ _ ).

~~Зачеркнутый текст~~ - обромление двумя волнистыми линиями (~~) зачеркивают текст.

## Цитаты 

Чтобы параграф отобразился как цитата, нужно поставить перед ним закрывающую угловую скобку (>).

> Если заблудился в лесу, иди домой.    
 (с) Стэтхем.

 ## Списки 

 В системе Markdown есть несколько видов списков. Для их оформления перед каждым пунктом нужно поставить подходящий тег и отделить его от текста пробелом.

 ### Нумерованные списки

 Для создания нумеровоного списка перед пунктами нужно поставить число с точкой.
 При этом нумирация в разметке ленивая. Неважно, какие именно числа вы напишете :
 Mardown пронумерует список автоматически.

 1. Пункт №1
 2. Пункт №2
 3. Пункт №3
 ***
 1. Пункт №1
 1. Пункт №2
 1. Пункт №3
 ***
 1. Пункт №1
 100. Пункт №2
 100000000. Пункт №3

### Ненумированные списки 
Для создание не нумированного списка нужно поставить перед каждым пунктом звездочку (*), дефис (-) или плюс (+).

 * Пункт №1
 + Пункт №2
 - Пункт №3


## Работа с изоброжениями.
### В Markdown :
Чтобы добавить изображение в текст, необходимо написать следующее :
***
![Текст который будет отоброжаться если картинка не загрузиться](markdown.png) - в скобочках ссылка на картинку.

## Работа с Git

#### Работа с любой программой всегда начинается с её настройки. Git можно настроить один раз и менять что-то только по мере необходимости.

#### Указать имя пользователя — git config --global user.name "Ivan Ivanov". Задаёт имя пользователя, от которого будут идти коммиты. Вместо Ivan Ivanov нужно написать свои данные на латинице. Если имя состоит из одного слова, кавычки можно не ставить.

#### Указать электронную почту — git config --global user.email "mail@gmail.com". Вместо mail@gmail.com нужно указать вашу почту. Обратите внимание, она должна совпадать с той, на которую зарегистрирован аккаунт в Гитхабе.

#### Посмотреть настройки — git config --list. Параметры можно посмотреть и в конфигурационном файле, но этот способ быстрее.

 ### Команды Git :

* `git add` - команда добавляет содержимое рабочей директории в индекс (staging area) для последующего коммита. По умолчанию git commit использует лишь этот индекс, так что вы можете использовать git add для сборки слепка вашего следующего коммита.

* `git status` - показывает состояния файлов в рабочей директории и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе. Вдобавок к этому выводятся подсказки о том, как изменить состояние файлов.

* `git diff` - используется для вычисления разницы между любыми двумя Git деревьями. Это может быть разница между вашей рабочей директорией и индексом (собственно git diff), разница между индексом и последним коммитом (git diff --staged), или между любыми двумя коммитами (git diff master branchB).

* `git difftool` - запускает внешнюю утилиту сравнения для показа различий в двух деревьях, на случай если вы хотите использовать что-либо отличное от встроенного просмотрщика git diff.

* `git commit` - берёт все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.

* `git reset` - используется в основном для отмены изменений. Она изменяет указатель HEAD и, опционально, состояние индекса. Также эта команда может изменить файлы в рабочей директории при использовании параметра --hard, что может привести к потере наработок при неправильном использовании, так что убедитесь в серьёзности своих намерений прежде чем использовать его.

* `git rm` - используется в Git для удаления файлов из индекса и рабочей директории. Она похожа на git add с тем лишь исключением, что она удаляет, а не добавляет файлы для следующего коммита.

* `git mv` - удобный способ переместить файл, а затем выполнить git add для нового файла и git rm для старого.

* `git clean` - используется для удаления мусора из рабочей директории. Это могут быть результаты сборки проекта или файлы конфликтов слияний.

Ветвление и слияние
* `git branch` - это своего рода “менеджер веток”. Она умеет перечислять ваши ветки, создавать новые, удалять и переименовывать их.

* `git checkout` - используется для переключения веток и выгрузки их содержимого в рабочую директорию.

* `git merge` - используется для слияния одной или нескольких веток в текущую. Затем она устанавливает указатель текущей ветки на результирующий коммит.

* `git mergetool` - вызывает внешнюю программу слияний, в случае если у вас возникли проблемы слияния.

* `git log` - используется для просмотра истории коммитов, начиная с самого свежего и уходя к истокам проекта. По умолчанию, она показывает лишь историю текущей ветки, но может быть настроена на вывод истории других, даже нескольких сразу, веток. Также её можно использовать для просмотра различий между ветками на уровне коммитов.

* `git stash` - используется для временного сохранения всех незакоммиченных изменений для очистки рабочей директории без необходимости коммитить незавершённую работу в новую ветку.

* `git tag` - используется для задания постоянной метки на какой-либо момент в истории проекта. Обычно она используется для релизов.

### Совместная работа и обновление проектов

> Не так уж много команд в Git требуют сетевого подключения для своей работы, практически все команды оперируют с локальной копией проекта. Когда вы готовы поделиться своими наработками, всего несколько команд помогут вам работать с удалёнными репозиториями.

* `git fetch` - связывается с удалённым репозиторием и забирает из него все изменения, которых у вас пока нет и сохраняет их локально.

* `git pull` - работает как комбинация команд git fetch и git merge, т.е. Git вначале забирает изменения из указанного удалённого репозитория, а затем пытается слить их с текущей веткой.

* `git push` - используется для установления связи с удалённым репозиторием, вычисления локальных изменений отсутствующих в нём, и собственно их передачи в вышеупомянутый репозиторий. Этой команде нужно право на запись в репозиторий, поэтому она использует аутентификацию.

* `git remote` - служит для управления списком удалённых репозиториев. Она позволяет сохранять длинные URL репозиториев в виде понятных коротких строк, например "origin", так что вам не придётся забивать голову всякой ерундой и набирать её каждый раз для связи с сервером. Вы можете использовать несколько удалённых репозиториев для работы и git remote поможет добавлять, изменять и удалять их.

* `git archive` - используется для упаковки в архив указанных коммитов или всего репозитория.

* `git submodule` - используется для управления вложенными репозиториями. 
Например, это могут быть библиотеки или другие, используемые не только в этом проекте ресурсы. У команды submodule есть несколько под-команд — add, update, sync и др. — для управления такими репозиториями.

***

## Системы контроля версий можно разделить на две группы:

1. Централизованные системы контроля версий;

2. Распределенные системы контроля версий.

Централизованная система контроля версий - это система, при которой репозиторий проекта хранится на сервере и вносить изменения вы можете непосредственно только в этот репозиторий при помощи специальных клиентских приложений. Среди таких систем можно выделить: ClearCase, TFVC, SVN.

Распределенная система контроля версий - это система, при которой копия репозитория может храниться на машине у каждого разработчика, что значительно снижает риск потерять результат работы над проектом. Примером таких систем могут быть: Git, Mercurial, Bazaar.

Git является распределенной системой контроля версий, разработанной Линусом Торвальдсом для управления разработкой ядра Linux. На данный момент Git завоевал огромную популярность в IT сообществе и, как следствие, его часто можно встретить в стеке технологий различных компаний.