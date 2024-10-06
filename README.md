## Система контроля версий Git.

__Система контроля версий__ - это система, записывающая изменения
в файле или наборе файлов в течение времени и позволяющая
возвращаться к определённой версии.

Одно или несколько изменений в системе контроля версий
называют __ревизией__ или __версией__. Каждая ревизия содержит информацию
о том, что изменилось, кто внёс изменения, когда это было и
комментарии к изменению.

Ключевые возможности:
- ведение истории всех изменений в виде отдельных версий кода
- управление записями
- анализ изменений

__Репозиторий__ - термин, который переводится с английского
repository как "хранилище". В нём хранятся все изменения проекта.

## Команды Git

Проверка наличия Git на компьютере:

'git --version'

Первоначальная настройка:

'git config --global user.name _username_'
'git config --global user.email _useremail_'
'git config --global coreignorecase false'

Просмотр настроек:

'git config --list'

Работа с репозиториями:

Создание репозитория производится вызовом команды 'git init'
в корневой папке проекта. Результатом данной операции должно
быть появление папки __.git__ в папке проекта.

Удаление папки __.git__ является удалением репозитория -
контроль версий прекращается. Через терминал это можно сделать
командой 'rm -rf .git', вызванной из папки проекта.

'git status' - текущее состояние репозитория
'git add _filename_' - добавить файл к отслеживаемым
'git add --all' - добавить несколько файлов
'git add .' - добавить всю текущую папку
'git commit -m _текст_' - зафиксировать изменения под названием,
указанном в тексте.
'git clone _repo_ _dir_' - копирует проект в указанную директорию.

Ветки:

Ветки в Git - отдельный поток разработки.
Основная, стабильная версия проекта хранится
в главной ветке - main.

'git branch' - просмотр ветки проекта.
'git branch _name_' - создание ветки с указанным именем.
'git branch -M _name_' - переименование текущей ветки.
'git checkout _name_' - переход на указанную ветку.
'git checkout -b _name_' - создание и переход на созданную ветку.
'git merge _name_' - делает слияние веток. Вызывается из целевой ветки
с указанием имени присоединяемой ветки.

Работа с удалёнными репозиториями:

'git remote add _origin_ _address_' - добавление ссылки на удалённый
репозиторий.
'git push -u _repo_ _branch_' - отправляет локальную ветку в удалённый
репозиторий и делает ветку основной для дальнейшей работы. После первого вызова
последующие вызовы команды можно делать сокращенно: 'git push'.
'git pull' - получает изменения из удалённого репозитория. Выполняет
две операции:
- 'git fetch' - скачивает изменения
- 'git merge' - вливает изменения в текущую рабочую версию
 
