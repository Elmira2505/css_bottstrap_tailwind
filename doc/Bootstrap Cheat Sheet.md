Вот тебе удобная шпаргалка CSS → Bootstrap 5. Я разделил её по категориям, чтобы ты могла использовать таблицу при переводе своих учебных проектов.

# CSS to Bootstrap 5 — Cheat Sheet

## 1. Display & Layout

| CSS                      | Bootstrap 5      | Назначение        |
| ------------------------ | ---------------- | ----------------- |
| `display: flex`          | `d-flex`         | Flexbox           |
| `display: block`         | `d-block`        | Блочный элемент   |
| `display: inline`        | `d-inline`       | Строчный элемент  |
| `display: inline-block`  | `d-inline-block` | Строчно-блочный   |
| `display: none`          | `d-none`         | Скрыть элемент    |
| `display: grid`          | `d-grid`         | CSS Grid          |
| `flex-direction: row`    | `flex-row`       | Горизонтально     |
| `flex-direction: column` | `flex-column`    | Вертикально       |
| `flex-wrap: wrap`        | `flex-wrap`      | Перенос элементов |
| `flex-wrap: nowrap`      | `flex-nowrap`    | Без переноса      |

## 2. Flexbox & Alignment

| CSS                              | Bootstrap 5               | Назначение            |
| -------------------------------- | ------------------------- | --------------------- |
| `justify-content: start`         | `justify-content-start`   | В начало              |
| `justify-content: center`        | `justify-content-center`  | По центру             |
| `justify-content: end`           | `justify-content-end`     | В конец               |
| `justify-content: space-between` | `justify-content-between` | Между элементами      |
| `justify-content: space-around`  | `justify-content-around`  | Вокруг элементов      |
| `align-items: start`             | `align-items-start`       | По верху              |
| `align-items: center`            | `align-items-center`      | По центру             |
| `align-items: end`               | `align-items-end`         | По низу               |
| `align-self: center`             | `align-self-center`       | Выравнивание элемента |
| `gap: 8px`                       | `gap-2`                   | Расстояние            |
| `gap: 16px`                      | `gap-3`                   | Расстояние            |
| `gap: 24px`                      | `gap-4`                   | Расстояние            |

## 3. Margin & Padding

Bootstrap использует систему spacing от 0 до 5.

| CSS                    | Bootstrap | Значение            |
| ---------------------- | --------- | ------------------- |
| `margin: 0`            | `m-0`     | 0                   |
| `margin: 8px`          | `m-2`     | 8px                 |
| `margin: 16px`         | `m-3`     | 16px                |
| `margin: 24px`         | `m-4`     | 24px                |
| `margin: 48px`         | `m-5`     | 48px                |
| `margin-top: 16px`     | `mt-3`    | Верхний отступ      |
| `margin-bottom: 24px`  | `mb-4`    | Нижний отступ       |
| `margin-left: 8px`     | `ms-2`    | Отступ слева в LTR  |
| `margin-right: 8px`    | `me-2`    | Отступ справа в LTR |
| `padding: 16px`        | `p-3`     | Внутренний отступ   |
| `padding: 24px`        | `p-4`     | Внутренний отступ   |
| `padding-top: 16px`    | `pt-3`    | Сверху              |
| `padding-bottom: 16px` | `pb-3`    | Снизу               |
| `padding-left: 24px`   | `ps-4`    | Слева в LTR         |
| `padding-right: 24px`  | `pe-4`    | Справа в LTR        |

## 4. Width & Height

| CSS                 | Bootstrap 5  | Назначение                |
| ------------------- | ------------ | ------------------------- |
| `width: 25%`        | `w-25`       | Ширина 25%                |
| `width: 50%`        | `w-50`       | Ширина 50%                |
| `width: 75%`        | `w-75`       | Ширина 75%                |
| `width: 100%`       | `w-100`      | Полная ширина             |
| `width: auto`       | `w-auto`     | Автоматическая ширина     |
| `height: 100%`      | `h-100`      | Высота 100%               |
| `height: 100vh`     | `vh-100`     | Высота экрана             |
| `min-height: 100vh` | `min-vh-100` | Минимальная высота экрана |
| `max-width: 100%`   | `mw-100`     | Максимальная ширина       |

## 5. Typography — текст

| CSS                          | Bootstrap 5                 | Назначение        |
| ---------------------------- | --------------------------- | ----------------- |
| `text-align: left`           | `text-start`                | Слева             |
| `text-align: center`         | `text-center`               | По центру         |
| `text-align: right`          | `text-end`                  | Справа            |
| `font-weight: 400`           | `fw-normal`                 | Обычный           |
| `font-weight: 500`           | `fw-medium`                 | Средний           |
| `font-weight: 600`           | `fw-semibold`               | Полужирный        |
| `font-weight: 700`           | `fw-bold`                   | Жирный            |
| `font-weight: 800`           | `fw-bolder`                 | Более жирный      |
| `font-style: italic`         | `fst-italic`                | Курсив            |
| `text-transform: uppercase`  | `text-uppercase`            | Заглавные буквы   |
| `text-transform: lowercase`  | `text-lowercase`            | Строчные буквы    |
| `text-decoration: underline` | `text-decoration-underline` | Подчёркивание     |
| `text-decoration: none`      | `text-decoration-none`      | Без подчёркивания |

## 6. Colors — цвета

| CSS                             | Bootstrap 5      |
| ------------------------------- | ---------------- |
| `color: white`                  | `text-white`     |
| `color: black`                  | `text-black`     |
| `color: gray`                   | `text-secondary` |
| `background-color: white`       | `bg-white`       |
| `background-color: black`       | `bg-black`       |
| `background-color: yellow`      | `bg-warning`     |
| `background-color: primary`     | `bg-primary`     |
| `background-color: transparent` | `bg-transparent` |

Важно: Bootstrap использует собственную цветовую палитру. Если нужен точный HEX-код из дизайна, оставляй собственный CSS.

## 7. Borders & Shadows

| CSS                        | Bootstrap 5      |
| -------------------------- | ---------------- |
| `border: 1px solid`        | `border`         |
| `border: none`             | `border-0`       |
| `border-top: 1px solid`    | `border-top`     |
| `border-bottom: 1px solid` | `border-bottom`  |
| `border-radius: 4px`       | `rounded-1`      |
| `border-radius: 8px`       | `rounded-3`      |
| `border-radius: 50%`       | `rounded-circle` |
| `border-radius: 0`         | `rounded-0`      |
| `box-shadow`               | `shadow`         |
| `box-shadow: none`         | `shadow-none`    |
| `box-shadow: small`        | `shadow-sm`      |
| `box-shadow: large`        | `shadow-lg`      |

## 8. Position

| CSS                  | Bootstrap 5         |
| -------------------- | ------------------- |
| `position: relative` | `position-relative` |
| `position: absolute` | `position-absolute` |
| `position: fixed`    | `position-fixed`    |
| `position: sticky`   | `position-sticky`   |
| `top: 0`             | `top-0`             |
| `bottom: 0`          | `bottom-0`          |
| `start: 0`           | `start-0`           |
| `end: 0`             | `end-0`             |
| `translate-middle`   | `translate-middle`  |

## 9. Responsive Design — адаптивность

Bootstrap использует специальные breakpoint-префиксы.

| Префикс      | Минимальная ширина |
| ------------ | ------------------ |
| Без префикса | 0px                |
| `sm`         | 576px              |
| `md`         | 768px              |
| `lg`         | 992px              |
| `xl`         | 1200px             |
| `xxl`        | 1400px             |

Примеры:

| CSS media query                               | Bootstrap                 |
| --------------------------------------------- | ------------------------- |
| На всех экранах `width: 100%`                 | `w-100`                   |
| От 768px `width: 50%`                         | `w-md-50`                 |
| Скрыть на мобильном                           | `d-none d-md-block`       |
| Показать только на мобильном                  | `d-block d-md-none`       |
| Вертикально на мобильном, горизонтально на ПК | `flex-column flex-md-row` |

## 10. Bootstrap Components

Это уже не просто замена CSS, а готовые компоненты.

| HTML / CSS                | Bootstrap         |
| ------------------------- | ----------------- |
| Обычная карточка          | `card`            |
| Внутренняя часть карточки | `card-body`       |
| Заголовок карточки        | `card-title`      |
| Текст карточки            | `card-text`       |
| Навигация                 | `navbar`          |
| Кнопка                    | `btn`             |
| Жёлтая кнопка             | `btn btn-warning` |
| Чёрная кнопка             | `btn btn-dark`    |
| Форма                     | `form-control`    |
| Выпадающий список         | `dropdown`        |
| Метка                     | `badge`           |
| Контейнер                 | `container`       |
| Строка Grid               | `row`             |
| Колонка                   | `col`             |

# 11. Самое важное: как переводить CSS в Bootstrap

Возьмём твой Blog Preview Card.

Было — CSS:

```
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 90vh;
}

.card {
  display: flex;
  flex-direction: column;
  padding: 24px;
  border-radius: 20px;
}
```

Стало — Bootstrap HTML:

```
<main class="min-vh-100 d-flex
             justify-content-center
             align-items-center">

  <div class="card flex-column p-4 rounded-4">
    Content
  </div>

</main>
```

Обрати внимание: `rounded-4` даёт 16px, а не 20px. Если тебе нужны точные 20px, оставляй собственный CSS.

## 12. Интерактивная практика

Попробуй подобрать Bootstrap-классы для этих CSS-свойств.

CSS → Bootstrap Quiz

5 вопросов

1\. display: flex

d-flex

flex-column

container



2\. justify-content: space-between

justify-content-center

justify-content-between

align-items-center



3\. padding: 24px

p-3

p-4

p-5



4\. border-radius: 50%

rounded-3

rounded-pill

rounded-circle



5\. font-weight: 700

fw-bold

fw-medium

fw-normal



Проверить ответы

Моя рекомендация: сохрани эту таблицу как свою Bootstrap Cheat Sheet. При переводе каждого проекта сначала ищи готовый Bootstrap utility class, а если его нет или он не соответствует дизайну — используй собственный CSS.

Официальная документация: [Bootstrap 5.3 Utilities](https://getbootstrap.com/docs/5.3/utilities/api/?utm_source=chatgpt.com) и [Bootstrap Components](https://getbootstrap.com/docs/5.3/components/?utm_source=chatgpt.com).