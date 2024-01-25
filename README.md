## Собственно, что нужно сделать?
Сейчас код сделан таким образом, что он меняет значение в  
 '.js-service-rating-td.td-1'  на 80 в блоке с шапкой "Основы государственности"(1 в таблице). Но код должен работать так, чтобы он менял значение на 80 в блоке с шапкой "Основной уровень"(4 в таблице). При этом в каждом из 4-х блоков таблицы есть '.js-service-rating-td.td-1'.

 ____

 Как я понимаю, нужно как-то сделать, чтобы в коде была ссылка на 4-й блок таблицы, чтобы он работал именно на него.


Так выглядит сама таблица
 ![Как выглядит таблица](https://github.com/SunriseSunshine/habrMonkey/blob/main/xOhfdE1ZsxI.jpg)
 

 Код первого блока таблицы(Основы государственности)
 ![Код первого блока таблицы](https://github.com/SunriseSunshine/habrMonkey/blob/main/HXVj0ulOisQ.jpg)


 Код второго блока таблицы(Основной уровень)
 ![Код первого блока таблицы](https://github.com/SunriseSunshine/habrMonkey/blob/main/1I0zHpdmgXA.jpg)

Код, который у меня есть, но его нужно доработать
(function() {
'use strict';

// Функция для изменения значения элемента
function changeValue(element, newValue) {
element.textContent = newValue;
}

// Изменяем значение элемента с классом "js-service-rating-td" на 80
var element1 = document.querySelector('.js-service-rating-td.td-1');
if (element1) {
changeValue(element1, '80');
}

// Изменяем значение элемента с классом "js-some-other-class" на 23
var element2 = document.querySelector('.js-some-other-class');
if (element2) {
changeValue(element2, '23');
}

// Сохраняем изменения в локальном хранилище для долгосрочного сохранения
if (element1 || element2) {
localStorage.setItem('customValue1', '80');
localStorage.setItem('customValue2', '23');
}
