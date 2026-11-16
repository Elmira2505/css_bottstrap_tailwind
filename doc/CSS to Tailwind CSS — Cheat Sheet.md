Вот твоя шпаргалка CSS → Tailwind CSS. Она построена по той же структуре, что и таблица CSS → Bootstrap, чтобы тебе было удобно сравнивать два фреймворка.

Tailwind работает немного иначе, чем Bootstrap: вместо готовых компонентов он предоставляет utility classes, из которых ты самостоятельно собираешь дизайн.

# CSS to Tailwind CSS — Cheat Sheet

## 1. Display & Layout

| CSS                      | Tailwind CSS   | Назначение        |
| ------------------------ | -------------- | ----------------- |
| `display: flex`          | `flex`         | Flexbox           |
| `display: block`         | `block`        | Блочный элемент   |
| `display: inline`        | `inline`       | Строчный элемент  |
| `display: inline-block`  | `inline-block` | Строчно-блочный   |
| `display: none`          | `hidden`       | Скрыть элемент    |
| `display: grid`          | `grid`         | CSS Grid          |
| `flex-direction: row`    | `flex-row`     | Горизонтально     |
| `flex-direction: column` | `flex-col`     | Вертикально       |
| `flex-wrap: wrap`        | `flex-wrap`    | Перенос элементов |
| `flex-wrap: nowrap`      | `flex-nowrap`  | Без переноса      |

## 2. Flexbox & Alignment

| CSS                              | Tailwind CSS      | Назначение            |
| -------------------------------- | ----------------- | --------------------- |
| `justify-content: start`         | `justify-start`   | В начало              |
| `justify-content: center`        | `justify-center`  | По центру             |
| `justify-content: end`           | `justify-end`     | В конец               |
| `justify-content: space-between` | `justify-between` | Между элементами      |
| `justify-content: space-around`  | `justify-around`  | Вокруг элементов      |
| `justify-content: space-evenly`  | `justify-evenly`  | Равные промежутки     |
| `align-items: start`             | `items-start`     | По верху              |
| `align-items: center`            | `items-center`    | По центру             |
| `align-items: end`               | `items-end`       | По низу               |
| `align-self: center`             | `self-center`     | Выравнивание элемента |
| `gap: 4px`                       | `gap-1`           | Расстояние            |
| `gap: 8px`                       | `gap-2`           | Расстояние            |
| `gap: 12px`                      | `gap-3`           | Расстояние            |
| `gap: 16px`                      | `gap-4`           | Расстояние            |
| `gap: 24px`                      | `gap-6`           | Расстояние            |

## 3. Margin & Padding

Tailwind использует spacing scale. В стандартной теме 1 единица соответствует 4px.

| CSS                    | Tailwind | Значение          |
| ---------------------- | -------- | ----------------- |
| `margin: 0`            | `m-0`    | 0                 |
| `margin: 4px`          | `m-1`    | 4px               |
| `margin: 8px`          | `m-2`    | 8px               |
| `margin: 12px`         | `m-3`    | 12px              |
| `margin: 16px`         | `m-4`    | 16px              |
| `margin: 24px`         | `m-6`    | 24px              |
| `margin: 32px`         | `m-8`    | 32px              |
| `margin-top: 16px`     | `mt-4`   | Сверху            |
| `margin-bottom: 24px`  | `mb-6`   | Снизу             |
| `margin-left: 8px`     | `ml-2`   | Слева             |
| `margin-right: 8px`    | `mr-2`   | Справа            |
| `padding: 16px`        | `p-4`    | Внутренний отступ |
| `padding: 24px`        | `p-6`    | Внутренний отступ |
| `padding-top: 16px`    | `pt-4`   | Сверху            |
| `padding-bottom: 16px` | `pb-4`   | Снизу             |
| `padding-left: 24px`   | `pl-6`   | Слева             |
| `padding-right: 24px`  | `pr-6`   | Справа            |

Дополнительно:

- `mx-auto` — горизонтальные margin auto.
- `my-4` — вертикальный margin 16px.
- `px-4` — горизонтальный padding 16px.
- `py-4` — вертикальный padding 16px.

## 4. Width & Height

| CSS                 | Tailwind CSS   | Назначение                |
| ------------------- | -------------- | ------------------------- |
| `width: 100%`       | `w-full`       | Полная ширина             |
| `width: 50%`        | `w-1/2`        | Половина ширины           |
| `width: 25%`        | `w-1/4`        | Четверть ширины           |
| `width: auto`       | `w-auto`       | Автоматическая ширина     |
| `width: 100vw`      | `w-screen`     | Ширина экрана             |
| `height: 100%`      | `h-full`       | Полная высота родителя    |
| `height: 100vh`     | `h-screen`     | Высота экрана             |
| `min-height: 100vh` | `min-h-screen` | Минимальная высота экрана |
| `max-width: 100%`   | `max-w-full`   | Максимальная ширина       |
| `max-width: 384px`  | `max-w-96`     | Максимальная ширина 384px |

## 5. Typography — текст

| CSS                          | Tailwind CSS     | Назначение           |
| ---------------------------- | ---------------- | -------------------- |
| `text-align: left`           | `text-left`      | Слева                |
| `text-align: center`         | `text-center`    | По центру            |
| `text-align: right`          | `text-right`     | Справа               |
| `font-weight: 400`           | `font-normal`    | Обычный              |
| `font-weight: 500`           | `font-medium`    | Средний              |
| `font-weight: 600`           | `font-semibold`  | Полужирный           |
| `font-weight: 700`           | `font-bold`      | Жирный               |
| `font-weight: 800`           | `font-extrabold` | Очень жирный         |
| `font-style: italic`         | `italic`         | Курсив               |
| `text-transform: uppercase`  | `uppercase`      | Заглавные буквы      |
| `text-transform: lowercase`  | `lowercase`      | Строчные буквы       |
| `text-decoration: underline` | `underline`      | Подчёркивание        |
| `text-decoration: none`      | `no-underline`   | Без подчёркивания    |
| `line-height: 1.5`           | `leading-normal` | Межстрочный интервал |

### Размеры текста

| CSS               | Tailwind    |
| ----------------- | ----------- |
| `font-size: 12px` | `text-xs`   |
| `font-size: 14px` | `text-sm`   |
| `font-size: 16px` | `text-base` |
| `font-size: 18px` | `text-lg`   |
| `font-size: 20px` | `text-xl`   |
| `font-size: 24px` | `text-2xl`  |
| `font-size: 30px` | `text-3xl`  |
| `font-size: 36px` | `text-4xl`  |
| `font-size: 48px` | `text-5xl`  |

## 6. Colors — цвета

| CSS                             | Tailwind CSS     |
| ------------------------------- | ---------------- |
| `color: white`                  | `text-white`     |
| `color: black`                  | `text-black`     |
| `color: gray`                   | `text-gray-500`  |
| `color: red`                    | `text-red-500`   |
| `color: blue`                   | `text-blue-500`  |
| `background-color: white`       | `bg-white`       |
| `background-color: black`       | `bg-black`       |
| `background-color: yellow`      | `bg-yellow-400`  |
| `background-color: blue`        | `bg-blue-500`    |
| `background-color: transparent` | `bg-transparent` |

Для точных цветов из дизайна можно использовать arbitrary values:

```
<div class="bg-[#f4d04e] text-[#111111]">
  My Card
</div>
```

## 7. Borders & Shadows

| CSS                        | Tailwind CSS   |
| -------------------------- | -------------- |
| `border: 1px solid`        | `border`       |
| `border: none`             | `border-0`     |
| `border-top: 1px solid`    | `border-t`     |
| `border-bottom: 1px solid` | `border-b`     |
| `border-radius: 4px`       | `rounded`      |
| `border-radius: 8px`       | `rounded-lg`   |
| `border-radius: 12px`      | `rounded-xl`   |
| `border-radius: 16px`      | `rounded-2xl`  |
| `border-radius: 50%`       | `rounded-full` |
| `border-radius: 0`         | `rounded-none` |
| `box-shadow: small`        | `shadow-sm`    |
| `box-shadow: normal`       | `shadow`       |
| `box-shadow: large`        | `shadow-lg`    |
| `box-shadow: none`         | `shadow-none`  |

Для нестандартной тени:

```
<div class="shadow-[8px_8px_0_#000]">
  Blog Card
</div>
```

## 8. Position

| CSS                  | Tailwind CSS      |
| -------------------- | ----------------- |
| `position: relative` | `relative`        |
| `position: absolute` | `absolute`        |
| `position: fixed`    | `fixed`           |
| `position: sticky`   | `sticky`          |
| `top: 0`             | `top-0`           |
| `bottom: 0`          | `bottom-0`        |
| `left: 0`            | `left-0`          |
| `right: 0`           | `right-0`         |
| `z-index: 10`        | `z-10`            |
| `overflow: hidden`   | `overflow-hidden` |
| `overflow: auto`     | `overflow-auto`   |

## 9. Responsive Design — адаптивность

Tailwind использует breakpoint-префиксы. Важно: Tailwind работает по принципу mobile-first.

| Префикс      | Минимальная ширина |
| ------------ | ------------------ |
| Без префикса | 0px                |
| `sm:`        | 640px              |
| `md:`        | 768px              |
| `lg:`        | 1024px             |
| `xl:`        | 1280px             |
| `2xl:`       | 1536px             |

Примеры:

| Задача                                        | Tailwind                           |
| --------------------------------------------- | ---------------------------------- |
| Полная ширина на всех экранах                 | `w-full`                           |
| Половина ширины от 768px                      | `md:w-1/2`                         |
| Скрыть на мобильном, показать от 768px        | `hidden md:block`                  |
| Показывать только на мобильном                | `block md:hidden`                  |
| Вертикально на мобильном, горизонтально на ПК | `flex flex-col md:flex-row`        |
| Разные размеры текста                         | `text-base md:text-xl lg:text-2xl` |
| Разные отступы                                | `p-4 md:p-6 lg:p-8`                |

## 10. Hover, Focus & Transitions

| CSS                           | Tailwind CSS           |
| ----------------------------- | ---------------------- |
| `cursor: pointer`             | `cursor-pointer`       |
| `:hover`                      | `hover:`               |
| `:focus`                      | `focus:`               |
| `:active`                     | `active:`              |
| `transition: all`             | `transition-all`       |
| `transition: colors`          | `transition-colors`    |
| `duration: 300ms`             | `duration-300`         |
| `opacity: 0`                  | `opacity-0`            |
| `opacity: 100%`               | `opacity-100`          |
| `transform: scale(1.05)`      | `hover:scale-105`      |
| `transform: translateY(-4px)` | `hover:-translate-y-1` |

Пример:

```
<button class="
  bg-black text-white
  px-6 py-3 rounded-lg
  hover:bg-gray-700
  transition-colors duration-300
">
  Learn More
</button>
```

## 11. CSS Grid

| CSS                                     | Tailwind CSS           |
| --------------------------------------- | ---------------------- |
| `display: grid`                         | `grid`                 |
| `grid-template-columns: 1fr 1fr`        | `grid-cols-2`          |
| `grid-template-columns: repeat(3, 1fr)` | `grid-cols-3`          |
| `grid-template-columns: repeat(4, 1fr)` | `grid-cols-4`          |
| `grid-template-columns: 1fr`            | `grid-cols-1`          |
| `grid-column: span 2`                   | `col-span-2`           |
| `grid-row: span 2`                      | `row-span-2`           |
| `gap: 16px`                             | `gap-4`                |
| `place-items: center`                   | `place-items-center`   |
| `place-content: center`                 | `place-content-center` |

## 12. Images

| CSS                       | Tailwind CSS     |
| ------------------------- | ---------------- |
| `width: 100%`             | `w-full`         |
| `height: 100%`            | `h-full`         |
| `object-fit: cover`       | `object-cover`   |
| `object-fit: contain`     | `object-contain` |
| `object-position: center` | `object-center`  |
| `border-radius: 50%`      | `rounded-full`   |
| `max-width: 100%`         | `max-w-full`     |

## 13. Что Tailwind не заменяет автоматически

Не все CSS-свойства имеют готовый utility class. Для них используются arbitrary values или собственный CSS.

| CSS                          | Tailwind                  |
| ---------------------------- | ------------------------- |
| `width: 384px`               | `w-[384px]`               |
| `height: 200px`              | `h-[200px]`               |
| `max-width: 384px`           | `max-w-[384px]`           |
| `border-radius: 20px`        | `rounded-[20px]`          |
| `box-shadow: 8px 8px 0 #000` | `shadow-[8px_8px_0_#000]` |
| `color: #6b6b6b`             | `text-[#6b6b6b]`          |
| `background: #f4d04e`        | `bg-[#f4d04e]`            |
| `line-height: 1.5`           | `leading-[1.5]`           |

# 14. Практический пример: твой Blog Preview Card

Возьмём твой оригинальный проект Frontend Mentor и перепишем его на Tailwind.

## Blog Preview Card

[html, css coding challenge solution](https://images.openai.com/static-rsc-4/TTXtqf1JQUUmDLpJJolGDIIfUXDs8Ue4XyknD5-214U3s9O9XkSlhd8TDtLf5NFOkPa2EJ54RlWsMx1DNXguCOXu1vInIW1-DPRVdzana6D1F_BaR_CMjY_PwEknhQH0hQACLOtbaMLqLrCCVvaYc_d3RFPkcXqaskEX3LDNiQA?purpose=inline)

[frontendmentor.io](https://www.frontendmentor.io/solutions/html-css-MuYTJJPcQp?utm_source=chatgpt.com)

Learning

Published 21 Dec 2023

HTML & CSS foundations

These languages are the backbone of every website, defining structure, content, and presentation.

[Blog-preview-card coding challenge solution | Frontend Mentor](https://images.openai.com/static-rsc-4/1Zrk2bcuPHx2-gwQ6ahL7vHid4Ncoc8QX4hcvR7I7OeX5NCT2rDhlFYiMetJxHbE9fWVT4ZD9qVse3aLvcljYAmPpTyLnMW_Qn2cy8-BUNL9YviDHptbrr4K4rFzAPMJclh8t9RUCDS9k1X71p-83_j5S2pMpN-rW_IDWCVsTIQ?purpose=inline)

Greg Hooper

HTML с Tailwind:

```

<main class="min-h-screen bg-[#f4d04e] flex flex-col justify-center items-center p-4">

  <article class="w-full max-w-96 bg-white border border-[#111] rounded-[20px] p-6 shadow-[8px_8px_0_#000]">

    <img
      src="./assets/images/illustration-article.svg"
      alt="Article illustration"
      class="w-full h-[200px] object-cover rounded-[10px]"
    >

    <span class="inline-block bg-[#f4d04e] text-[#111] text-sm font-extrabold px-3 py-1 rounded mt-6 mb-3">
      Learning
    </span>

    <p class="text-base mb-3">
      Published 21 Dec 2023
    </p>

    <h1 class="text-2xl font-extrabold mb-3">
      HTML & CSS foundations
    </h1>

    <p class="text-[#6b6b6b] mb-6">
      These languages are the backbone of every website,
      defining structure, content, and presentation.
    </p>

    <div class="flex items-center gap-3">
      <img
        src="./assets/images/image-avatar.webp"
        alt="Greg Hooper"
        class="w-8 h-8 rounded-full"
      >

      <span class="font-bold">
        Greg Hooper
      </span>
    </div>

  </article>

</main>

```

Обрати внимание: здесь мы практически полностью отказались от отдельного CSS-файла. Все стили находятся непосредственно в `class`.

# 15. Сравнение CSS, Bootstrap и Tailwind

Это полезно запомнить, поскольку ты изучаешь сразу три подхода.

| Задача       | CSS                       | Bootstrap                | Tailwind         |
| ------------ | ------------------------- | ------------------------ | ---------------- |
| Flexbox      | `display: flex`           | `d-flex`                 | `flex`           |
| Column       | `flex-direction: column`  | `flex-column`            | `flex-col`       |
| Center       | `justify-content: center` | `justify-content-center` | `justify-center` |
| Padding 24px | `padding: 24px`           | `p-4`                    | `p-6`            |
| Margin 16px  | `margin: 16px`            | `m-3`                    | `m-4`            |
| Bold         | `font-weight: 700`        | `fw-bold`                | `font-bold`      |
| Rounded      | `border-radius: 50%`      | `rounded-circle`         | `rounded-full`   |
| Shadow       | `box-shadow`              | `shadow`                 | `shadow`         |
| Hidden       | `display: none`           | `d-none`                 | `hidden`         |
| Grid         | `display: grid`           | `d-grid`                 | `grid`           |

# 16. Проверь свои знания

Tailwind CSS Quiz

5 вопросов

1\. Какой класс Tailwind соответствует display: flex?

d-flex

flex

flex-row

2\. Какой класс соответствует flex-direction: column?

flex-column

flex-col

flex-direction-column

3\. Какой класс задаёт padding: 24px?

p-4

p-6

p-8

4\. Как сделать круглую картинку?

rounded-lg

rounded-xl

rounded-full

5\. Как показать элемент только на экранах от 768px?

hidden md:block

block md:hidden

md:hidden

Проверить ответы

## Официальная документация

- [Tailwind CSS Documentation](https://tailwindcss.com/docs?utm_source=chatgpt.com)
- [Styling with Utility Classes](https://tailwindcss.com/docs/styling-with-utility-classes?utm_source=chatgpt.com)
- [Responsive Design](https://tailwindcss.com/docs/responsive-design?utm_source=chatgpt.com)
- [Hover, Focus and States](https://tailwindcss.com/docs/hover-focus-and-other-states?utm_source=chatgpt.com)

Мой совет для твоего обучения: попробуй сделать Blog Preview Card в трёх вариантах: чистый CSS, Bootstrap и Tailwind. Так ты на практике увидишь разницу между обычным CSS, компонентным подходом Bootstrap и utility-first подходом Tailwind.
