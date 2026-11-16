# CSS to Material UI (MUI) — Cheat Sheet

Вот четвёртая шпаргалка в твоей серии: CSS → Material UI (MUI).

Важное отличие: CSS, Bootstrap и Tailwind в основном работают со стилями HTML-элементов, а Material UI — это React component library. Ты используешь готовые React-компоненты и настраиваешь их через `sx`, props и theme.

Например:

- CSS: `display: flex`
- Bootstrap: `d-flex`
- Tailwind: `flex`
- MUI: `display: "flex"` внутри `sx`

MUI особенно полезен, когда ты разрабатываешь React-приложения: Dashboard, CRM, Admin Panel, формы и личные кабинеты.

## 1. Display & Layout

| CSS                      | Material UI (`sx`)        | Назначение        |
| ------------------------ | ------------------------- | ----------------- |
| `display: flex`          | `display: "flex"`         | Flexbox           |
| `display: block`         | `display: "block"`        | Блочный элемент   |
| `display: inline`        | `display: "inline"`       | Строчный элемент  |
| `display: inline-block`  | `display: "inline-block"` | Строчно-блочный   |
| `display: none`          | `display: "none"`         | Скрыть элемент    |
| `display: grid`          | `display: "grid"`         | CSS Grid          |
| `flex-direction: row`    | `flexDirection: "row"`    | Горизонтально     |
| `flex-direction: column` | `flexDirection: "column"` | Вертикально       |
| `flex-wrap: wrap`        | `flexWrap: "wrap"`        | Перенос элементов |
| `flex-wrap: nowrap`      | `flexWrap: "nowrap"`      | Без переноса      |

Пример:

```
<Box
  sx={{
    display: "flex",
    flexDirection: "column",
    alignItems: "center",
    justifyContent: "center",
  }}
>
  Content
</Box>
```

## 2. Flexbox & Alignment

| CSS                              | Material UI (`sx`)                |
| -------------------------------- | --------------------------------- |
| `justify-content: flex-start`    | `justifyContent: "flex-start"`    |
| `justify-content: center`        | `justifyContent: "center"`        |
| `justify-content: flex-end`      | `justifyContent: "flex-end"`      |
| `justify-content: space-between` | `justifyContent: "space-between"` |
| `justify-content: space-around`  | `justifyContent: "space-around"`  |
| `align-items: flex-start`        | `alignItems: "flex-start"`        |
| `align-items: center`            | `alignItems: "center"`            |
| `align-items: flex-end`          | `alignItems: "flex-end"`          |
| `align-self: center`             | `alignSelf: "center"`             |
| `gap: 8px`                       | `gap: 1`                          |
| `gap: 16px`                      | `gap: 2`                          |
| `gap: 24px`                      | `gap: 3`                          |

В MUI `gap: 1` обычно означает 8px, если используется стандартная тема со spacing 8px.

## 3. Margin & Padding

MUI использует `sx` и spacing-систему темы.

| CSS                    | Material UI (`sx`) | Значение          |
| ---------------------- | ------------------ | ----------------- |
| `margin: 0`            | `m: 0`             | 0                 |
| `margin: 8px`          | `m: 1`             | 8px               |
| `margin: 16px`         | `m: 2`             | 16px              |
| `margin: 24px`         | `m: 3`             | 24px              |
| `margin: 32px`         | `m: 4`             | 32px              |
| `margin-top: 16px`     | `mt: 2`            | Сверху            |
| `margin-bottom: 24px`  | `mb: 3`            | Снизу             |
| `margin-left: 8px`     | `ml: 1`            | Слева             |
| `margin-right: 8px`    | `mr: 1`            | Справа            |
| `padding: 16px`        | `p: 2`             | Внутренний отступ |
| `padding: 24px`        | `p: 3`             | Внутренний отступ |
| `padding-top: 16px`    | `pt: 2`            | Сверху            |
| `padding-bottom: 16px` | `pb: 2`            | Снизу             |
| `padding-left: 24px`   | `pl: 3`            | Слева             |
| `padding-right: 24px`  | `pr: 3`            | Справа            |

Обрати внимание: MUI spacing по умолчанию равен 8px, поэтому `p: 3` — это 24px.

## 4. Width & Height

| CSS                 | Material UI (`sx`)   | Назначение            |
| ------------------- | -------------------- | --------------------- |
| `width: 100%`       | `width: "100%"`      | Полная ширина         |
| `width: 50%`        | `width: "50%"`       | Половина ширины       |
| `width: auto`       | `width: "auto"`      | Автоматическая ширина |
| `width: 100vw`      | `width: "100vw"`     | Ширина экрана         |
| `height: 100%`      | `height: "100%"`     | Высота родителя       |
| `height: 100vh`     | `height: "100vh"`    | Высота экрана         |
| `min-height: 100vh` | `minHeight: "100vh"` | Минимальная высота    |
| `max-width: 384px`  | `maxWidth: 384`      | Максимальная ширина   |
| `min-width: 300px`  | `minWidth: 300`      | Минимальная ширина    |

Пример:

```
<Box
  sx={{
    width: "100%",
    maxWidth: 384,
    minHeight: "100vh",
    mx: "auto",
  }}
>
  Content
</Box>
```

## 5. Typography — текст

В MUI для текста можно использовать `Typography`.

| CSS                          | Material UI                   |
| ---------------------------- | ----------------------------- |
| `font-size: 12px`            | `fontSize: 12`                |
| `font-size: 16px`            | `fontSize: 16`                |
| `font-size: 24px`            | `fontSize: 24`                |
| `font-weight: 400`           | `fontWeight: 400`             |
| `font-weight: 500`           | `fontWeight: 500`             |
| `font-weight: 600`           | `fontWeight: 600`             |
| `font-weight: 700`           | `fontWeight: 700`             |
| `font-style: italic`         | `fontStyle: "italic"`         |
| `text-align: center`         | `textAlign: "center"`         |
| `text-transform: uppercase`  | `textTransform: "uppercase"`  |
| `text-transform: lowercase`  | `textTransform: "lowercase"`  |
| `text-decoration: underline` | `textDecoration: "underline"` |
| `line-height: 1.5`           | `lineHeight: 1.5`             |
| `letter-spacing: 1px`        | `letterSpacing: 1`            |

Пример:

```
<Typography
  variant="h4"
  sx={{
    fontWeight: 700,
    textAlign: "center",
    color: "#111111",
  }}
>
  My Blog
</Typography>
```

### Готовые Typography variants

| MUI variant | Назначение                |
| ----------- | ------------------------- |
| `h1`        | Главный заголовок         |
| `h2`        | Заголовок второго уровня  |
| `h3`        | Заголовок третьего уровня |
| `h4`        | Заголовок                 |
| `h5`        | Небольшой заголовок       |
| `h6`        | Маленький заголовок       |
| `subtitle1` | Подзаголовок              |
| `subtitle2` | Маленький подзаголовок    |
| `body1`     | Основной текст            |
| `body2`     | Дополнительный текст      |
| `caption`   | Мелкий текст              |
| `overline`  | Текст над заголовком      |

Важно: `variant` определяет типографический стиль, а не обязательно HTML-тег. Для семантики можно дополнительно указать `component="h1"`.

## 6. Colors — цвета

В MUI можно использовать палитру темы или собственные HEX-цвета.

| CSS                             | Material UI (`sx`)            |
| ------------------------------- | ----------------------------- |
| `color: white`                  | `color: "white"`              |
| `color: black`                  | `color: "black"`              |
| `color: gray`                   | `color: "text.secondary"`     |
| `color: primary`                | `color: "primary.main"`       |
| `color: secondary`              | `color: "secondary.main"`     |
| `color: error`                  | `color: "error.main"`         |
| `background-color: white`       | `bgcolor: "background.paper"` |
| `background-color: black`       | `bgcolor: "#000"`             |
| `background-color: primary`     | `bgcolor: "primary.main"`     |
| `background-color: yellow`      | `bgcolor: "warning.main"`     |
| `background-color: transparent` | `bgcolor: "transparent"`      |

Пример с собственными цветами:

```
<Box
  sx={{
    bgcolor: "#f4d04e",
    color: "#111111",
  }}
>
  My Card
</Box>
```

## 7. Borders & Shadows

| CSS                        | Material UI (`sx`)    |
| -------------------------- | --------------------- |
| `border: 1px solid`        | `border: 1`           |
| `border: none`             | `border: 0`           |
| `border-top: 1px solid`    | `borderTop: 1`        |
| `border-bottom: 1px solid` | `borderBottom: 1`     |
| `border-radius: 4px`       | `borderRadius: 1`     |
| `border-radius: 8px`       | `borderRadius: 2`     |
| `border-radius: 16px`      | `borderRadius: 2`     |
| `border-radius: 50%`       | `borderRadius: "50%"` |
| `box-shadow`               | `boxShadow: 1`        |
| `box-shadow: large`        | `boxShadow: 10`       |
| `box-shadow: none`         | `boxShadow: "none"`   |

Для точного дизайна:

```
<Box
  sx={{
    border: "1px solid #111",
    borderRadius: "20px",
    boxShadow: "8px 8px 0 #000",
  }}
>
  Blog Card
</Box>
```

Важно: `borderRadius: 2` в MUI по умолчанию обычно равен 8px, а `borderRadius: 3` — 12px. Это не такая же система, как у Tailwind или Bootstrap.

## 8. Position

| CSS                  | Material UI (`sx`)     |
| -------------------- | ---------------------- |
| `position: relative` | `position: "relative"` |
| `position: absolute` | `position: "absolute"` |
| `position: fixed`    | `position: "fixed"`    |
| `position: sticky`   | `position: "sticky"`   |
| `top: 0`             | `top: 0`               |
| `bottom: 0`          | `bottom: 0`            |
| `left: 0`            | `left: 0`              |
| `right: 0`           | `right: 0`             |
| `z-index: 10`        | `zIndex: 10`           |
| `overflow: hidden`   | `overflow: "hidden"`   |
| `overflow: auto`     | `overflow: "auto"`     |

Пример:

```
<Box
  sx={{
    position: "relative",
    width: 300,
  }}
>
  <Box
    sx={{
      position: "absolute",
      top: 0,
      right: 0,
      zIndex: 10,
    }}
  >
    Badge
  </Box>
</Box>
```

## 9. Responsive Design — адаптивность

MUI использует breakpoint-префиксы через объект `sx`.

Стандартные breakpoints MUI:

| MUI  | Минимальная ширина |
| ---- | ------------------ |
| `xs` | 0px                |
| `sm` | 600px              |
| `md` | 900px              |
| `lg` | 1200px             |
| `xl` | 1536px             |

Примеры:

| CSS                                           | Material UI                                  |
| --------------------------------------------- | -------------------------------------------- |
| Ширина 100%                                   | `width: "100%"`                              |
| От 900px ширина 50%                           | `width: { xs: "100%", md: "50%" }`           |
| Скрыть на мобильном                           | `display: { xs: "none", md: "block" }`       |
| Вертикально на мобильном, горизонтально на ПК | `flexDirection: { xs: "column", md: "row" }` |
| Разные размеры текста                         | `fontSize: { xs: 16, md: 24 }`               |
| Разные отступы                                | `p: { xs: 2, md: 4 }`                        |

Пример:

```
<Box
  sx={{
    display: "flex",
    flexDirection: {
      xs: "column",
      md: "row",
    },
    gap: {
      xs: 2,
      md: 4,
    },
  }}
>
  Content
</Box>
```

Здесь:

- `xs` — мобильные устройства.
- `md` — планшеты и большие экраны от 900px.
- При увеличении экрана направление меняется с `column` на `row`.

## 10. Hover, Focus & Transitions

| CSS                      | Material UI (`sx`)         |
| ------------------------ | -------------------------- |
| `cursor: pointer`        | `cursor: "pointer"`        |
| `:hover`                 | `"&:hover"`                |
| `:focus`                 | `"&:focus"`                |
| `:active`                | `"&:active"`               |
| `opacity: 0`             | `opacity: 0`               |
| `opacity: 1`             | `opacity: 1`               |
| `transition: all 0.3s`   | `transition: "all 0.3s"`   |
| `transform: scale(1.05)` | `transform: "scale(1.05)"` |

Пример:

```
<Button
  sx={{
    bgcolor: "#111",
    color: "#fff",
    transition: "all 0.3s",

    "&:hover": {
      bgcolor: "#555",
      transform: "scale(1.05)",
    },
  }}
>
  Learn More
</Button>
```

## 11. CSS Grid

| CSS                                     | Material UI (`sx`)                      |
| --------------------------------------- | --------------------------------------- |
| `display: grid`                         | `display: "grid"`                       |
| `grid-template-columns: 1fr 1fr`        | `gridTemplateColumns: "1fr 1fr"`        |
| `grid-template-columns: repeat(3, 1fr)` | `gridTemplateColumns: "repeat(3, 1fr)"` |
| `grid-template-columns: 1fr`            | `gridTemplateColumns: "1fr"`            |
| `grid-column: span 2`                   | `gridColumn: "span 2"`                  |
| `grid-row: span 2`                      | `gridRow: "span 2"`                     |
| `gap: 16px`                             | `gap: 2`                                |
| `place-items: center`                   | `placeItems: "center"`                  |
| `place-content: center`                 | `placeContent: "center"`                |

Пример:

```
<Box
  sx={{
    display: "grid",
    gridTemplateColumns: {
      xs: "1fr",
      md: "repeat(2, 1fr)",
      lg: "repeat(3, 1fr)",
    },
    gap: 3,
  }}
>
  <Box>Card 1</Box>
  <Box>Card 2</Box>
  <Box>Card 3</Box>
</Box>
```

## 12. Images

| CSS                       | Material UI (`sx`)         |
| ------------------------- | -------------------------- |
| `width: 100%`             | `width: "100%"`            |
| `height: 100%`            | `height: "100%"`           |
| `object-fit: cover`       | `objectFit: "cover"`       |
| `object-fit: contain`     | `objectFit: "contain"`     |
| `object-position: center` | `objectPosition: "center"` |
| `border-radius: 50%`      | `borderRadius: "50%"`      |
| `max-width: 100%`         | `maxWidth: "100%"`         |

MUI также предоставляет компонент `Avatar`:

```
<Avatar
  src="/images/avatar.webp"
  alt="Greg Hooper"
  sx={{
    width: 32,
    height: 32,
  }}
/>
```

## 13. Готовые компоненты Material UI

Здесь главное отличие от обычного CSS: MUI предоставляет готовые React-компоненты.

| HTML / CSS        | Material UI component  | Назначение              |
| ----------------- | ---------------------- | ----------------------- |
| `<div>`           | `Box`                  | Универсальный контейнер |
| Flexbox container | `Stack`                | Расположение элементов  |
| Card              | `Card`                 | Карточка                |
| Card content      | `CardContent`          | Контент карточки        |
| `<button>`        | `Button`               | Кнопка                  |
| `<input>`         | `TextField`            | Поле ввода              |
| `<form>`          | `Box component="form"` | Форма                   |
| `<img>`           | `CardMedia`            | Медиа в карточке        |
| Avatar image      | `Avatar`               | Аватар                  |
| Badge / Label     | `Chip`                 | Метка                   |
| Navigation        | `AppBar`               | Верхняя панель          |
| Navigation links  | `Toolbar`              | Панель инструментов     |
| Dialog            | `Dialog`               | Модальное окно          |
| Dropdown          | `Menu`                 | Выпадающее меню         |
| Table             | `Table`                | Таблица                 |
| Checkbox          | `Checkbox`             | Флажок                  |
| Radio button      | `Radio`                | Переключатель           |

# 14. Практический пример: Blog Preview Card на MUI

Перепишем твой Frontend Mentor проект на React + Material UI.

Сначала установи библиотеку в React-проект:

```
npm install @mui/material @emotion/react @emotion/styled
```

Основные импорты:

```
import {
  Box,
  Card,
  CardContent,
  CardMedia,
  Typography,
  Avatar,
  Chip,
} from "@mui/material";
```

Пример компонента BlogCard.jsx:

```

import {
  Box,
  Card,
  CardContent,
  CardMedia,
  Typography,
  Avatar,
  Chip,
} from "@mui/material";

function BlogCard() {
  return (
    <Box
      sx={{
        minHeight: "100vh",
        bgcolor: "#f4d04e",
        display: "flex",
        justifyContent: "center",
        alignItems: "center",
        p: 2,
      }}
    >
      <Card
        sx={{
          width: "100%",
          maxWidth: 384,
          p: 3,
          border: "1px solid #111",
          borderRadius: "20px",
          boxShadow: "8px 8px 0 #000",
        }}
      >
        <CardMedia
          component="img"
          image="./assets/images/illustration-article.svg"
          alt="Article illustration"
          sx={{
            height: 200,
            borderRadius: "10px",
            objectFit: "cover",
          }}
        />

        <CardContent sx={{ px: 0, pb: "0 !important" }}>

          <Chip
            label="Learning"
            sx={{
              bgcolor: "#f4d04e",
              color: "#111",
              fontWeight: 800,
              borderRadius: "4px",
              mb: 2,
            }}
          />

          <Typography variant="body2" sx={{ mb: 2 }}>
            Published 21 Dec 2023
          </Typography>

          <Typography
            variant="h5"
            component="h1"
            sx={{
              fontWeight: 800,
              mb: 2,
            }}
          >
            HTML & CSS foundations
          </Typography>

          <Typography
            variant="body1"
            sx={{
              color: "#6b6b6b",
              mb: 3,
            }}
          >
            These languages are the backbone of every
            website, defining structure, content,
            and presentation.
          </Typography>

          <Box
            sx={{
              display: "flex",
              alignItems: "center",
              gap: 1.5,
            }}
          >
            <Avatar
              src="./assets/images/image-avatar.webp"
              alt="Greg Hooper"
              sx={{ width: 32, height: 32 }}
            />

            <Typography fontWeight={700}>
              Greg Hooper
            </Typography>
          </Box>

        </CardContent>
      </Card>
    </Box>
  );
}

export default BlogCard;

```

# 15. Сравнение CSS, Bootstrap, Tailwind и MUI

Это твоя общая таблица для изучения четырёх технологий.

| Задача         | CSS                       | Bootstrap                | Tailwind         | MUI                        |
| -------------- | ------------------------- | ------------------------ | ---------------- | -------------------------- |
| Flexbox        | `display: flex`           | `d-flex`                 | `flex`           | `display: "flex"`          |
| Column         | `flex-direction: column`  | `flex-column`            | `flex-col`       | `flexDirection: "column"`  |
| Center         | `justify-content: center` | `justify-content-center` | `justify-center` | `justifyContent: "center"` |
| Padding 24px   | `padding: 24px`           | `p-4`                    | `p-6`            | `p: 3`                     |
| Margin 16px    | `margin: 16px`            | `m-3`                    | `m-4`            | `m: 2`                     |
| Bold           | `font-weight: 700`        | `fw-bold`                | `font-bold`      | `fontWeight: 700`          |
| Rounded circle | `border-radius: 50%`      | `rounded-circle`         | `rounded-full`   | `borderRadius: "50%"`      |
| Shadow         | `box-shadow`              | `shadow`                 | `shadow`         | `boxShadow: 1`             |
| Hidden         | `display: none`           | `d-none`                 | `hidden`         | `display: "none"`          |
| Grid           | `display: grid`           | `d-grid`                 | `grid`           | `display: "grid"`          |
| Hover          | `:hover`                  | `:hover`                 | `hover:`         | `"&:hover"`                |

# 16. Когда использовать каждую технологию?

[File:Devicon-css3-plain.svg - Wikimedia Commons](https://images.openai.com/static-rsc-4/avKn6C8AYr4Td5gULdPj8_La409PzwnM59x56qrQ7Utt5kM7Pq8fMr9arUARw7XgZZMIgP8HqowQYRy9xAhOqHyyP4ZgZvWBRl4UZsx5_aF7VYUg5azk3RBYykS_EGuNW0yyB80Hrt3VMhvH8zOO0uZEawIhLD_EEzIWMA-QZBo?purpose=inline)

CSS

Полный контроль над стилями. Подходит для любого сайта.

[Conrad Booker](https://images.openai.com/static-rsc-4/YcnGMBOH7ZFqQu6kBfG5fEXSPgtkt7gtRqOqU2FY2t3eX61ZkZ-AVHonrD9jCQa-TCbDu5L87gLQQ3Xd0wENhwF78LEb32mYS9VQqfZH--Uixx0A3y8aFrBxyN6aJ3X6KWGGGa0wVMID-p7K3oCkcUkjoIoKmSen5NirSKjPlBw?purpose=inline)

Bootstrap

Быстрая разработка сайтов с готовыми компонентами и сеткой.

[Logo Tailwind CSS – Logos PNG](https://images.openai.com/static-rsc-4/p2CaJ-lTaLliSDsT11iqWnIoGte3Nn-TqPb9vx0DnyG3pNRUFwKyiTrRHTwujxkE6-RzemIctP2lxY9E0XJeCNWCKYEUVo0TyTjc4LaSTeziWZAyyGkkz-wN5Ks1fjXzGErpQ9TRRBN7BQ3LHCxkpLKHwRbW6Cr8Hq8vCvRr4x0?purpose=inline)

Tailwind CSS

Создание уникального дизайна непосредственно в HTML/JSX через utility classes.

[Material UI Logo PNG Vector (SVG) Free Download](https://images.openai.com/static-rsc-4/SbPAW5-akkjgACMtsmyu64joZ5UvCtyrnFpBvzc4W0upC5WC-3Ac4RMWGswvPCrX5Hc64Ju6XmV7ISBGocsq9GCWSPwfBhY5dGeYv3GBnqa4A0GS2_FGmxFzKc887QaiOXsKBAfcyABDnuVqQ5ku6MdDKFPTwA4AhT7izuwSfHE?purpose=inline)

Material UI

Готовые React-компоненты для сложных интерфейсов, Dashboard, CRM и приложений.

## 17. Официальная документация

- [MUI — Getting Started](https://mui.com/material-ui/getting-started/?utm_source=chatgpt.com)
- [MUI — The sx prop](https://mui.com/system/getting-started/the-sx-prop/?utm_source=chatgpt.com)
- [MUI — Box](https://mui.com/material-ui/react-box/?utm_source=chatgpt.com)
- [MUI — Card](https://mui.com/material-ui/react-card/?utm_source=chatgpt.com)
- [MUI — Responsive Breakpoints](https://mui.com/material-ui/customization/breakpoints/?utm_source=chatgpt.com)

Моя рекомендация для твоего обучения: поскольку ты уже работаешь с React, попробуй один и тот же Blog Preview Card реализовать на всех четырёх технологиях. Это даст тебе хорошее понимание того, как устроена современная frontend-разработка.

И запомни главное: MUI — это не просто CSS-классы, а библиотека готовых React-компонентов. Поэтому при переходе на MUI ты меняешь не только CSS, но и способ построения интерфейса.
