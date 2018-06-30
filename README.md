# SameHeight for jQuery

jQuery плагин для выравнивания элементов по высоте

> For english scroll below

## Зачем нужен

Часто при отображении информации в несколько колонок нужно выровнять кнопки и картинки по одной линии.
Плагин делает одинаковой высоту у тех элементов, высота которых непредсказуема.

Было:

![Было](https://nukinuki.github.io/sameheight/img/before.png)

Стало:

![Стало](https://nukinuki.github.io/sameheight/img/after.png) 

## Как использовать

1. Скачайте или клонируйте этот репозиторий:
```
git clone git@github.com:nukinuki/sameheight.git
```

2. Положите файл `jquery.sameheight.js` из папки `dist` в ваш проект.

3. Подключите скрипт в вашем html _после_ подключения jQuery: 
```
<script src="/your-path-to-js/jquery.sameheight.js" />
```

или

Подключите его через CDN:
```
<script src="https://cdn.jsdelivr.net/gh/nukinuki/sameheight@0.1/dist/jquery.sameheight.js" />
```

4. Укажите аттрибут `data-height-group="название_группы"` у всех элементов, высота которых должна быть одинаковой.

Скрипт работает автоматически, обновляет высоту после ресайза и не мешает адаптиву.

## Пример

https://jsfiddle.net/Nukinuki/gywLf7ca/

## Команды

Все команды запускаются через `$.sameheight('команда');`. Например `$.sameheight('update');`.

### update

Принудительное обновление высоты, например при нажатии на кнопку "Показать ещё".

Также скрипт слушает событие: `$(document).trigger('sameheightupdaterequired');`

### disable

Cнимает установленные ранее высоты элементов. Скрипт перестаёт слушать события.

### enable

Делает update, включает события.


# ENGLISH

jQuery plugin for aligning elements 

## What it does

It aligns images, texts and buttons on the same line in multi-column layout.
Actually it just makes height of marked elements equal.

Before:

![Было](https://nukinuki.github.io/sameheight/img/before.png)

After:

![Стало](https://nukinuki.github.io/sameheight/img/after.png) 

## How to use

1. Download or clone this repository:
```
git clone git@github.com:nukinuki/sameheight.git
```

2. Copy `jquery.sameheight.js` from `dist` folder to your project.

3. Add the script in your HTML markup _after_ jQuery: 
```
<script src="/your-path-to-js/jquery.sameheight.js" />
```

or

Use the CDN link:
```
<script src="https://cdn.jsdelivr.net/gh/nukinuki/sameheight@0.1/dist/jquery.sameheight.js" />
```

4. Set attribute `data-height-group="name_of_the_group"` of all elements, that require to be of same height.

Nothing else required, script just works. It updates heights after every window resize and doesn't mess with responsiveness.

## Example

https://jsfiddle.net/Nukinuki/gywLf7ca/

## Actions

All actions are executed through `$.sameheight('action');`. Like `$.sameheight('update');`.

### update

Updates heights, for example after clicking on "Show more" button.

Another way is to trigger the event on document: `$(document).trigger('sameheightupdaterequired');`

### disable

Removes all height overrides from elements, stops listen to events.

### enable

Do update action, starts to listen to events again.
