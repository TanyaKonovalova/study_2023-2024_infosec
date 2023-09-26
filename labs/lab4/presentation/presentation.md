---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №4
author: Коновалова Татьяна Борисовна
institute: РУДН, Москва, Россия

date: 26 Сентября 2023

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: xelatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Презентация по лабораторной работы №4

## Цель лабораторной работы №4

Цель: Получить навыки работы в консоли с расширенными атрибутами файлов

## Задачи лабораторной работы №4

- Определить расширенные атрибуты файла в Виртуальной машине;
- Установка расширенного атрибута "a" на файл;
- Снять расширенные атрибуты "a" с файла.

# Ход выполнения лабораторной работы

## Просмотр расширенных атрибутов 

- От имени пользователя guest просматрела расширенные атрибуты файла;
- При попытке добавить расширенный атрибут выдаёт ошибку.

![Просмотр расширенных атрибутов](image/1.png){ #fig:001 width=70% }

## Изменение расширенных атрибутов

- От имени администратора добавила расширенный атрибут a;
- Также убедилась в корректном установлении атрибута с помощью команды lsattr.

![Проверка корректнсти установки атрибута +a](image/3.png){ #fig:003 width=70% }

## Проверка действий

- Дописала в файл информацию командой echo >> и проверила выполнение командой cat;
- При попытке удаления информации из файла, переименования файла и смены атрибутов выдаёт ошибку. 

![Проверка действий при наличии атрибута a](image/4.png){ #fig:004 width=70% }

## Проверка действий

- Через администратора убрала атрибут а;
- Теперь не возникает ошибки при удалении информации из файла, переименовании файла и смене атрибутов --- действия спокойно выполняются.

![Проверка действий при отсутствии атрибута а](image/5.png){ #fig:005 width=70% }

## Проверка действий

- Через администратора добавила атрибут i;
- Прочитала файл командой cat;
- При попытке дозаписи в файл, удалиния информации из файла, переименования файла и смены атрибутов получила ошибку.

![Проверка действий при наличии атрибута i](image/7.png){ #fig:007 width=70% }

## Выводы

Приобрела практические навыки работы с расширенными атрибутами файлов через консоль, опробовала на практике действия с файлами с установленными на них расширенными атрибутами a и i

## Библиография

СПИСОК ЛИТЕРАТУРЫ

1.Медведовский И.Д., Семьянов П.В., Платонов В.В. Атака через Internet. — НПО "Мир и семья-95",  1997. — URL: http://bugtraq.ru/library/books/attack1/index.html

2.Запечников С. В. и др. Информационн~пасность открытых систем. Том 1. — М.: Горячаая линия -Телеком, 2006.

СПИСОК ИНТЕРНЕТ-ИСТОЧНИКОВ

1.[Электронный ресурс] - доступ: https://debianinstall.ru/diskretsionnoe-razgranichenie-dostupa-linux/

## {.standout}

Спасибо за внимание!
