# LR6
Лабораторная работа №6

Цель лабораторной работы: изучение базовых возможностей системы
управления версиями, опыт работы с Git Api, опыт работы с локальным и
удаленным репозиторием.

## Содержание
1. [Форк репозитория LR6](#форк-репозитория-lr6)
2. [Установка Git](#установка-git)
3. [Клонирование репозитория](#клонирование-репозитория)
4. [Добавление файла в GitHub и подтягивание изменений](#добавление-файла-в-github-и-подтягивание-изменений)
5. [История операций для каждой из веток](#история-операций-для-каждой-из-веток)
6. [Просмотр последних изменений](#просмотр-последних-изменений)
7. [Слияние веток и разрешение конфликтов](#слияние-веток-и-разрешение-конфликтов)
8. [Удаление побочной ветки](#удаление-побочной-ветки)
9. [Откат коммита](#откат-коммита)
10. [Создание ветки для отчёта](#создание-ветки-для-отчёта)
11. [История операций в отчёте](#история-операций-в-отчёте)
12. [Выводы](#выводы)

## Форк репозитория LR6
1. Переходим на страницу репозитория [LR6](https://github.com/Kurtyanik/LR6)

2. Нажимаем кнопку "Fork" в правом верхнем углу страницы.

## Установка Git
1. Скачиваем установщик Git с [официального сайта](https://git-scm.com/).

2. Запускаем установщик и следуем инструкциям.

3. Настраиваем имя пользователя и email:
```bash
git config --global user.name "Saraev K.S. 4417"
git config --global user.email Kssaraev@gmail.com
```

## Клонирование репозитория
1. Клонируем репозиторий на локальную машину:
```bash
git clone https://github.com/rippyik/LR6.git
```

## Добавление файла в GitHub и подтягивание изменений
1. Нажатием кнопки "Add file" -> "Upload files" добавляем файл в репози!
торий.

2. Подтягиваем изменения на локальную машину:
```bash
git pull
```

## История операций для каждой из веток
1. Получил историю коммитов для всех веток с помощью команды:
```bash
git log --all --graph --decorate --oneline
```

<img width="873" height="152" alt="Снимок" src="https://github.com/user-attachments/assets/9150a3e4-4b54-47d3-a5a0-1d08ad00fc12" />

## Просмотр последних изменений
1. Для просмотра изменений последнего коммита выполнил:
```bash
git log -p -1
```

<img width="1144" height="398" alt="Снимок1" src="https://github.com/user-attachments/assets/35cedc5e-1d3c-4b1d-a6d3-c705823ee0f8" />

## Слияние веток и разрешение конфликтов
1. Переключился на ветку `master`:
```bash
git checkout master
```

2. Вывел список веток:
```bash
git branch -a
```

<img width="504" height="174" alt="Снимок2" src="https://github.com/user-attachments/assets/1c30686e-349f-424d-a1e3-66a903574f47" />


3. Создал два файла conflict.txt с разным содержимым для создания конфликта

<img width="813" height="296" alt="Снимок3" src="https://github.com/user-attachments/assets/c460b6de-5af8-46a8-b20f-8b3558b17703" />
<img width="882" height="315" alt="Снимок4" src="https://github.com/user-attachments/assets/724889fc-74d7-4a21-9ba5-02e68d5cd0e7" />

4. Слил ветку `feature` в ветку `master`:
```bash
git merge feature
```

5. Разрешил конфликт в файле [conflict.txt](conflict.txt)(принял версию из ветки `feature`).

<img width="815" height="315" alt="Снимок5" src="https://github.com/user-attachments/assets/99a89761-03a6-4280-bdc2-f7ca909e7747" />

## Удаление побочной ветки
1. Убедился, что нахожусь в ветке `master`.

2. Удалил локальную ветку:
```bash
git branch -d feature
```

3. Удалил удаленную ветку:
```bash
git push origin --delete feature
```

<img width="665" height="178" alt="Снимок6" src="https://github.com/user-attachments/assets/deed7b17-c322-4ba1-a7c2-c30da1f44a90" />

## Откат коммита
1. Получил историю коммитов:
```bash
git log --oneline
```

<img width="945" height="220" alt="Снимок7" src="https://github.com/user-attachments/assets/209ffe49-8c11-45da-8c4c-700ced957354" />

2. Отменил изменения коммита, добавляющего useless.txt, при помощи revert:
```bash
git revert a0d9119
```

<img width="553" height="123" alt="Снимок8" src="https://github.com/user-attachments/assets/6f63f44e-e034-423c-8c7e-3770a43a5f07" />

## Создание ветки для отчёта
1. Создал новую ветку report и переключился на неё:
```bash
git checkout -b report
```
2. Добавление папки со скриншотами.

<img width="1042" height="304" alt="Снимок9" src="https://github.com/user-attachments/assets/17d28c1b-b03c-46c8-95d8-2eb0a4c1aa03" />

## История операций в отчёте
1. Получил историю коммитов в форматированном виде и добавил её в отчёт:
```bash
git log --pretty=format:"%h - %ad - %an - %s" --date=format:"%d.%m.%Y %H:%M:%S"
```

<img width="1212" height="269" alt="Снимок10" src="https://github.com/user-attachments/assets/0a646ecf-a43e-47c9-a29e-befe0fd70ccd" />

## Вывод
В данной лабораторной работе были изучены базовые возможности системы управления версиями, был получен опыт работы с Git Api и опыт работы с локальным и удаленным репозиторие, также был получен опыт работы с Markdown
