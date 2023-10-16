---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №8
author: Коновалова Татьяна Борисовна
institute: РУДН, Москва, Россия

date: 23 Октября 2023

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

# Элементы криптографии. Шифрование (кодирование) различных исходных текстов одним ключом

## Цель лабораторной работы №8

Цель лабораторной работы --- Освоить на практике применение однократного гаммирования при работе с различными текстами на одном ключе.

## Задачи лабораторной работы

1.Не зная ключа и не стремясь его определить, прочитать оба исходных текста;
2.Разработать приложение, позволяющее шифровать и дешифровать тексты в режиме однократного гаммирования;
3.Определить и выразить аналитически способ, при котором злоумышленник может прочитать оба текста, не зная ключа и не стремясь его определить.

# Ход лабораторной работы №8

## Теоретическое введение

Гаммирование представляет собой наложение (снятие) на открытые (зашифрованные) данные последовательности элементов других данных, полученной с помощью некоторого криптографического алгоритма, для получения зашифрованных (открытых) данных. Иными словами, наложение
гаммы — это сложение её элементов с элементами открытого (закрытого)
текста по некоторому фиксированному модулю, значение которого представляет собой известную часть алгоритма шифрования.

## Функция шифрования

Cоздала функцию, которая осуществляет однократное гаммирование посредством побитового XOR

![Функция шифрования](image/1.png){ #fig:001 width=70% }

## Исходные данные

Задала две равные по длине текстовые строки и создала случайный символьный ключ такой же длины

![Исходные данные](image/2.png){ #fig:002 width=70% }

## Исходные данные

![Случайный символьный ключ](image/3.png){ #fig:003 width=70% }

## Шифрование данных

Осуществила шифрование двух текстов по ключу с помощью написанной функции

![Шифрование данных](image/4.png){ #fig:004 width=70% }

## Получение данных без ключа

Создала переменную, которая, прогнав два шифрованных текста через побитовый XOR, поможет злоумышленнику получить один текст, зная другой, без ключа

![Получение данных без ключа](image/5.png){ #fig:005 width=70% }

## Получение данных без ключа

![Получение данных без ключа](image/6.png){ #fig:006 width=70% }

## Получение части данных

Таким же способом я получила часть данных из исходных предложений

![Получение части данных](image/7.png){ #fig:007 width=70% }

## Выводы

Освоила на практике применение однократного гаммирования при работе с различными текстами на одном ключе

## Библиография

СПИСОК ЛИТЕРАТУРЫ

1.Медведовский И.Д., Семьянов П.В., Платонов В.В. Атака через Internet. — НПО "Мир и семья-95",  1997. — URL: http://bugtraq.ru/library/books/attack1/index.html

2.Теоретические знания, приведённые в Лабораторной работе №8 - https://esystem.rudn.ru/pluginfile.php/2090135/mod_resource/content/2/008-lab_crypto-key.pdf


СПИСОК ИНТЕРНЕТ-ИСТОЧНИКОВ

1.[Электронный ресурс] - доступ: https://codeby.school/blog/informacionnaya-bezopasnost/razgranichenie-dostupa-v-linux-znakomstvo-s-astra-linux


## {.standout}

Спасибо за внимание!
