# Einzelwerk assignment

## Как посмотреть работу

Сборщиком Vite был создан продакшн билд, который размещен на GitHub Pages, [онлайн посмотреть и протестировать форму можно тут](https://idcso.github.io/einzelwerk-assignment/).

Для запуска проекта локально:

1. клонировать репозиторий
2. npm install
3. npm run dev

## Примененный стек

- React / TypeScript
- React Hook Form
- Zod
- react-dropzone / react-select / react-input-mask
- Tailwind CSS
- Vite

## Выполнено по ТЗ

- [x] Валидация всех полей форм, в том числе и типов загружаемых документов. В случае ошибки, данные с формы не отправляются и выводится ошибка под соответствующими полями. Сами поля с ошибками подсвечиваются.
- [x] Вывод всех данных в консоль при отправке формы
- [x] Возможность выбора нескольких вариантов в селекте
- [x] Настройка проекта под дальнейшее расширение

## Дополнительная информация

Структура проекта была создана на основе методологии FSD, что предоставляет отличные возможности для дальнейшего его расширения и рефакторинга. Вся форма находится в слое `features` и состоит из нескольких компонентов, которые "изолированы" в этом слое, на выход же отдается только один основной компонент через паблик апи. Написаны кастомные UI-компоненты в разделе `src/shared/ui`, в которых отсутствует какая-либо бизнес-логика и которые можно использовать во всех частях (слоях) проекта. По итогу получаем чистые `App.tsx` и основную страницу `MainPage` без логики внутри себя, в которых просто собираются нужные виджеты и фичи.

### Пару слов о форме

Отдельное поле для загрузки файлов было сделано при помощи модального окна (по макету не до конца было понятно, как именно задумывалось это). Модальное окно можно закрыть нажатием на любую область вокруг поля загрузки, либо нажатием на клавишу `esc`. Загрузить файлы можно кликом по полю загрузки либо просто перетащить файлы в поле drag-n-drop. Можно за раз загружать несколько файлов, дозагрузить файлы к уже загруженным, удалять загруженные файлы. В поле ввода телефона можно вводить только цифры. По макету в селекте используется другой шрифт, но он платный, поэтому был использован основной шрифт формы.

## Демонстрация различных состояний формы

- ![Скриншот пустой формы](https://i.imgur.com/mGx3QeK.png)
- ![Скриншот заполненной формы](https://i.imgur.com/hrnfLQ6.png)
- ![Скриншот формы с ошибками валидации](https://i.imgur.com/AVD35XV.png)
