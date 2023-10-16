---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №7
author: Коновалова Татьяна Борисовна
institute: РУДН, Москва, Россия

date: 16 Октября 2023

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

# Элементы криптографии. Однократное гаммирование

## Цель лабораторной работы №7

Цель лабораторной работы --- Освоить основы шифрования через однократное гаммирование.

## Задачи лабораторной работы №7

1.Подобрать ключ, чтобы получить сообщение «С Новым Годом, друзья!»;
2.Разработать приложение, позволяющее шифровать и дешифровать данные в режиме однократного гаммирования.

# Ход лабораторной работы №7

## Теоретическое введение

Гаммирование представляет собой наложение (снятие) на открытые (зашифрованные) данные последовательности элементов других данных, полученной с помощью некоторого криптографического алгоритма, для получения зашифрованных (открытых) данных. Иными словами, наложение
гаммы — это сложение её элементов с элементами открытого (закрытого)
текста по некоторому фиксированному модулю, значение которого представляет собой известную часть алгоритма шифрования.

## Функция шифрования

Создала функцию, которая осуществляет однократное гаммирование посредством побитового XOR

![Функция шифрования](image/1.png){ #fig:001 width=70% }

## Исходные данные

Задала текстовую строку и случайный символьный ключ такой же длины 

![Исходные данные](image/3.png){ #fig:003 width=70% }

## Результат работы программы

Запустила функцию. В первом случае получила зашифрованный текст. 
После этого, используя тот же самый ключ, осуществила дешифровку текста.
Так же, зная оригинальный текст и его шифорку, с помощью кода могу получить ключ.

![Результат работы программы](image/4.png){ #fig:004 width=70% }

## Выводы

Освоила основы шифрования через однократное гаммирование

## Библиография

СПИСОК ЛИТЕРАТУРЫ

1.Медведовский И.Д., Семьянов П.В., Платонов В.В. Атака через Internet. — НПО "Мир и семья-95",  1997. — URL: http://bugtraq.ru/library/books/attack1/index.html

2.Теоретические знания, приведённые в Лабораторной работе №7 - https://esystem.rudn.ru/pluginfile.php/2090133/mod_resource/content/2/007-lab_crypto-gamma.pdf


СПИСОК ИНТЕРНЕТ-ИСТОЧНИКОВ

1.[Электронный ресурс] - доступ: https://codeby.school/blog/informacionnaya-bezopasnost/razgranichenie-dostupa-v-linux-znakomstvo-s-astra-linux


## {.standout}

Спасибо за внимание!
