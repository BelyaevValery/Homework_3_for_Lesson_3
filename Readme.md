# Инструкция по работе с GIT

## Что такое GIT

GIT - одна из реализаций распределенных систем контроля версий, имеющая как локальную версионность, так и версионнось на сервере. GIT является самой популярной системой контроля версий на сегодняшний день.

## Подготовка репозитория

Для того, чтобы создать репозиторий в указанной папке используется команда *git init*. Для этого достаточно написать команду *git init* в папке с будущим репозиторием.

## Создание "сохранений"

### Просмотр информации об изменениях

Для того, чтобы посмотреть информацию об изменениях, сделанных в текущей ветке, необходимо использовать команду *git status*. Для этого достаточно использовать *git status* в папке с репозиторием.

### Добавление файла к коммиту

Для того, чтобы добавить файл к новому коммиту ("сохранению") необходимо использовать команду *git add*. Используется она следующим образом: в папке с репозиторием пишем команду *git add <имя_файла>*

### Создание коммитов

Для создания новой фиксации необходимо использовать команду *git commit*. Используется она следующим образом: в папке с репозиторием пишется команда *git commit -m "<сообщение к коммиту>"*. Все файлы коммита должны быть предворительно добавлены с помощью команды *git add*. Сообщение коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Перемещение между сохранениями

Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с репозиторием следующим образом: *git checkout <номер коммита>*

## Журнал изменений

Для того, чтобы посмотреть журнал изменений, необходимо использовать команду *git log*. Для этого достаточно использовать *git log* в папке с репозиторием. Для отображения данной команды в графическом виде, необходимо добавить параметр *git log --graph*.

## Ветки в GIT

Основная ветка проекта называется *master*. Для создания новой ветки (ответвления) необходимо использовать команду *git branch*. Используется она следующим образом: в папке с репозиторием пишем команду *git branch <имя_ветки>*. Для перемещения между ветками (ответвлениями) необходимо использовать команду *git checkout*. Используется она следующим образом: пишем команду *git checkout <имя_ветки>*

## Слияние веток и разрешение конфликтов

Слияние используется в Git, чтобы собрать воедино разветвленную историю. С помощью команды *git merge* выполняет слияние отдельных направлений разработки, созданных с помощью команды *git branch*, в единую ветку. При вызове команды *git merge <имя_ветки>* произойдет слияние указанной функциональной ветки с текущей. При попытке объединить ветки, в которых изменена одна и та же часть того же файла, Git не сможет сделать выбор между версиями. В таком случае операция останавливается прямо перед созданием коммита слияния, чтобы пользователь вручную разрешил конфликты.

## Удаление веток

Для того чтобы удалить локальную ветку в Git нужно выполнить команду *git branch -d <имя_ветки>*. Если возникают ошибки и предупреждения то для принудительного удаления ветки можно воспользоваться опцией -D: *git branch -D <имя_ветки>*.