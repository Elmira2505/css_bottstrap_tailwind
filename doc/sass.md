Давай подробно изучим Sass (SCSS) на примере твоего QR Code Component из Frontend Mentor.

Sass — это расширение CSS, которое позволяет писать стили более удобно, структурированно и с возможностью повторного использования кода.

Главное: Sass не заменяет CSS. Он компилируется в обычный CSS, который понимает браузер.

## 1. CSS vs Sass

Посмотри, как один и тот же стиль выглядит в CSS и Sass.

Обычный CSS:

```
.card {
  background: white;
  padding: 16px;
  border-radius: 16px;
}

.card img {
  width: 100%;
}

.card h1 {
  font-size: 24px;
}
```

Sass (SCSS):

```
.card {
  background: white;
  padding: 16px;
  border-radius: 16px;

  img {
    width: 100%;
  }

  h1 {
    font-size: 24px;
  }
}
```

Обрати внимание на вложенность (Nesting).

В Sass тебе не нужно каждый раз повторять `.card`.

## 2. Основные возможности Sass

### A. Variables — переменные

В CSS переменные обычно начинаются с `--`, а в Sass — с `$`.

```
$primary-color: #3685ff;
$text-color: #1f3251;
$card-radius: 20px;

.card {
  background: white;
  border-radius: $card-radius;
}

h1 {
  color: $text-color;
}
```

Зачем нужны?

Если ты захочешь поменять основной цвет проекта, достаточно изменить переменную в одном месте.

### B. Nesting — вложенность

Позволяет группировать стили по компонентам.

```
.card {
  padding: 20px;

  img {
    width: 100%;
  }

  h1 {
    font-size: 24px;
    color: #1f3251;
  }

  p {
    font-size: 15px;
    color: gray;
  }
}
```

### C. Mixins — повторное использование стилей

Представь, что у тебя есть несколько элементов, которые нужно центрировать.

```
@mixin center-content {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  @include center-content;
}

.card {
  @include center-content;
}
```

`@mixin` — создаёт набор стилей.

`@include` — подключает этот набор там, где он нужен.

### D. Partials — разделение файлов

Можно разделить стили на несколько файлов:

```
scss/
│
├── _variables.scss
├── _mixins.scss
├── _card.scss
├── _footer.scss
└── style.scss
```

В главном файле `style.scss`:

```
@use "variables";
@use "mixins";
@use "card";
@use "footer";
```

Это помогает поддерживать порядок в больших проектах.

## 3. Практика: переписываем твой QR Code Component на Sass

[GitHub - Epirito/qr-code-component: This is a solution to the QR code component challenge on Frontend Mentor · GitHub](https://images.openai.com/static-rsc-4/6BtAsMndq89XrQ0SLbxRVQUJNuCGuHcDSepBrLujlB1u_jXL9BAo2GzHdDokJli-002jubxqZTAr2_YZkgXYeLKIWKuCdifVckpHt13gfzUlnOyUxvmZExwAaocOusqcEKJjcRvMigg4TuHc-78T7WfFUZAYZ2U1vtVSg0iF5d0?purpose=inline)

[github.com](https://github.com/Epirito/qr-code-component?utm_source=chatgpt.com)

Структура проекта:

```
qr-code/
│
├── index.html
├── images/
│   └── image-qr-code.png
│
└── scss/
    ├── _variables.scss
    ├── _card.scss
    ├── _footer.scss
    └── style.scss
```

Файл `_variables.scss`:

```
$background-color: #d5e1ef;
$card-color: #ffffff;
$heading-color: #1f314f;
$text-color: #68778d;

$card-width: 320px;
$border-radius: 20px;
```

Файл `_card.scss`:

```
@use "variables" as v;

.card {
  width: v.$card-width;
  padding: 16px;
  background: v.$card-color;
  border-radius: v.$border-radius;
  text-align: center;

  img {
    width: 100%;
    border-radius: 12px;
  }

  h1 {
    margin-top: 24px;
    font-size: 24px;
    color: v.$heading-color;
  }

  p {
    margin-top: 16px;
    color: v.$text-color;
    font-size: 15px;
  }
}
```

Файл `_footer.scss`:

```
.attribution {
  margin-top: 24px;
  text-align: center;
  font-size: 12px;

  a {
    color: blue;
  }
}
```

Главный файл `style.scss`:

```
@use "variables" as v;
@use "card";
@use "footer";

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  min-height: 100vh;
  background: v.$background-color;
}

.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 24px;
}
```

## 4. Как подключить Sass к проекту

Если ты используешь Vite, открой терминал:

```
npm install -D sass
```

Переименуй файл:

```
style.css → style.scss
```

В `index.html` подключи его через JavaScript (например, в `src/main.js`):

```
import './scss/style.scss';
```

Vite автоматически скомпилирует Sass в CSS при запуске проекта:

```
npm run dev
```

## 5. Проверим, что ты поняла

Sass — Mini Test

4 / 4

1\. Как объявляется переменная в Sass?

\--primary-color

$primary-color

var(primary-color)

Correct!

В Sass переменные начинаются с символа $.

2\. Что делает Nesting?

Создаёт базу данных

Позволяет вкладывать CSS-селекторы друг в друга

Заменяет HTML

Correct!

Nesting помогает группировать стили внутри родительского селектора.

3\. Для чего нужен @mixin?

Для повторного использования набора стилей

Для подключения JavaScript

Для создания HTML-элемента

Correct!

Mixin позволяет определить стили один раз и подключать их через @include.

4\. Что браузер получает после компиляции Sass?

SCSS

JavaScript

Обычный CSS

Correct!

Браузер не понимает Sass напрямую. Ему нужен обычный CSS.

Check answers

## Your score: 4 / 4

Try again

Моя рекомендация: сначала хорошо освой четыре вещи: Variables, Nesting, Mixins и Partials. Это фундамент Sass, который пригодится при разработке React-проектов.