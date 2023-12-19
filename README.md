# Домашнее задание #3

# Инструкция использования системы контроля версий.

## 4 шага работы с контролем версий:

1. Внести изменения
2. Сохранить изменения.
3. Добавить файлы с изменениями.
4. Зафиксировать эти изменения.

## Слияние веток:

- git merge BRANCH_NAME - слияние ветки BRANCH_NAME в текущую.

- git rebase BRANCH_NAME - слияние, посредством копирования коммитов и их перемещения из текущей ветки в ветку BRANCH_NAME.
  (Преимущество rebase над merge в том, что c помощью rebase можно делать чистые и красивые линейные последовательности коммитов. История коммитов будет чище, если применяется rebase).

  git rebase автоматически обновляет текущую ветку веткой BRANCH_NAME и перемещает её на вершину (конец) ветки BRANCH_NAME.

  После выполнения git rebase нужно сделать обратный git rebase из ветки BRANCH_NAME в ветку, из которой был сделан первый rebase.
  Так как ветка BRANCH_NAME является предком ветки, из которой был сделан rebase, git просто сдвигает ссылку на main вперёд к ветке BRANCH_NAME.

## Конфликты при слиянии веток:

Конфилкты возникают, когда затронуто общее рабочее пространство.

## Настройка удалённого репозитория:

1. Создать аккаунт на Github.com.
2. Создать локальный репозиторий.
3. Создать удалённый репозиторий.
4. Связать локальный и удалённый репозитории посредством ввода предложенных команд.
5. git push - отправить локальные изменения в удалённый репозиторий.
6. git pull - получить изменения из удалённого репозитория.

## Практика

https://learngitbranching.js.org/
