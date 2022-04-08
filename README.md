# salute-demo-app

Это небольшое Todo приложение (добавление, выполнение и удаление задач. [См. видео](https://youtu.be/P-o2rwHhARo)) демонстрирует пример взаимодействия с [Assistant Client](https://github.com/sberdevices/assistant-client). Для работы необходимо создать **два** проекта: один "SmartApp Code" и еще один - смартап в "SmartApp Studio", затем сгенерировать token и запустить проект.

## Создание проекта "SmartApp Code":

1. Идём на страницу SmartMarket Studio ([ссылка](https://developers.sber.ru/studio.));
1. В меню слева нажимаем "Создать проект";
2. Выбираем "Инструменты разработки приложений" -> Code (Инструменты разработки приложений)
1.1. Указываем "Название проекта";
1.1. В "Выбор шаблона" указываем "Пустой проект";
1.1. Нажимаем "Создать проект";
5. Переходим на страницу с проектами ([ссылка](https://smartapp-code.sberdevices.ru/));
6. Заходим в сам проект, переходим в пункт меню "Настройки проекта" (внизу меню), потом на закладку "Экспорт/Импорт", нажимаем на "Прикрепите файл" ~~В меню проекта (кнопка "⋮") выбираем "Загрузить";~~
7. Выбираеv архив "scenario-example.zip" (лежит в корне этого проекта) -  не весь проект из Git, только zip-файл, который внутри этого проекта;
8. Нажимаем "Сценарии";
9. Нажимаем "Собрать";
10. Нажимаем "Публикации";
11. Нажимаем "Получить вебхук" (URL на Webhook в буфере обмена).

## Создание смартапа в "SmartApp Studio":

1. Идём на страницу SmartApp Studio ([ссылка](https://developers.sber.ru/studio/) ~~[старая ссылка](https://smartapp-studio.sberdevices.ru/)~~);
1. Нажимаем "Создать смартап";
1. Указываем "Название смартапа" (указываем это же название в файле ".env.sample", в строке "REACT_APP_SMARTAPP"),  переименовываем его в ".env";
1. Переключаем "Выбор типа смартапа" на "Canvas App";
~~1. Переключаем "Выбор инструмента" на "Есть готовое приложение";~~
1. Нажимаем "Создать смартап".
1. ~~Либо~~ выбираем SmartApp Code API  и указываем URL на "Webhook" (полученный в "SmartApp Code")~~, либо выбираем SmartApp Code App и выбираем название и версию (в последующем версии нужно будет менять)~~;
1. Указываем URL на "Frontend Endpoint" (url страницы, где будет размещаться клиентская часть вашего приложения. **Для локального запуска не используется, можете указать любой)**;

## Генерация token:

1. Идём на страницу SmartApp Studio ([ссылка](https://developers.sber.ru/studio/) ~~[старая ссылка](https://smartapp-studio.sberdevices.ru/)~~);
1. В меню пользователя (правый верхний угол) выбираем "Настройки профиля";
1. Нажимаем "Эмулятор"~~"Auth Token"~~;
1. Нажимаем "Обновить ключ";
1. Нажимаем "Скопировать ключ" (сейчас token в буфере);
1. Указываем токен в файле ".env.sample", в строке "REACT_APP_TOKEN".
1. Переименовываем файл ".env.sample" в ".env".

## Запуск проекта:

```bash
npm install

npm start
```
~
