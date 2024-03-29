callbackRC - это модуль, который устанавливает виджет обратного звонка от RedConnect.

## Настройка собственного виджета

Чтобы настроить свой виджет на собственном сайте нужно зарегистрироваться в сервисе RedConnect. Для этого заполни форму на [этой странице](https://redconnect.ru/) и получи логин и пароль на свой почтовый ящик. После этого используя логин и пароль войди в личный кабинет на сайте [redconnect.ru](https://redconnect.ru/), выбери тариф и получи код для сайта. Код нужно вставить в файл `callbackRC.html`.

## Подключение компонента

Каталог с компонентом рекомендуется разместить в проекте по адресу `src/components/`. Обычно компонент подключается к проекту либо в шаблоне страницы, либо в шаблоне сайта. Так, если компонент подключается в шаблон страницы `index.pug`, а структура проекта следующая:

```
...
|-src
  ...
  |-components
    |-callbackRC
      callbackRC.html
      README.md
    ...
  ...
  |-pages
    ...
    |-home
      |+images
      index.js
      index.pug
      index.scss
    ...
  ...
...
package.json
...
```

то в нужное место файла `src/pages/home/index.pug` необходимо вставить команду:

```pug
include ../../components/callbackRC/callbackRC.html
```
