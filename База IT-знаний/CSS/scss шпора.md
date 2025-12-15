Сделаю тебе шпаргалку по **SCSS** — коротко и по блокам, чтобы можно было держать под рукой.

---

## 🟢 **Переменные**

```scss
$primary: #3498db;
$padding: 1rem;

.button {
  color: $primary;
  padding: $padding;
}
```

---

## 🟡 **Вложенность**

```scss
nav {
  ul {
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    text-decoration: none;
  }
}
```

---

## 🔵 **Миксины (mixins)**

```scss
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.box {
  @include flex-center;
}
```

---

## 🟣 **Расширения (extends)**

```scss
%btn-base {
  padding: 10px;
  border-radius: 5px;
}

.btn-primary {
  @extend %btn-base;
  background: blue;
}
```

---

## 🟠 **Функции**

```scss
@function double($n) {
  @return $n * 2;
}

.box {
  width: double(10px);
}
```

---

## 🟤 **Операции**

```scss
.box {
  width: 100% - 20px;
  height: 50px * 2;
}
```

---

## ⚪ **Импорт**

```scss
@use "variables";
@use "mixins" as m;

.box {
  @include m.flex-center;
}
```

---

## ⚫ **Условные конструкции**

```scss
@mixin theme($mode) {
  @if $mode == light {
    background: white;
    color: black;
  } @else {
    background: black;
    color: white;
  }
}

body {
  @include theme(dark);
}
```

---

## 🟤 **Циклы**

```scss
@for $i from 1 through 3 {
  .m-#{$i} {
    margin: #{$i * 5}px;
  }
}

@each $color in red, green, blue {
  .#{$color}-bg {
    background: $color;
  }
}
```

---

Хочешь, я соберу тебе **ультракомпактную шпаргалку SCSS на одной странице** (только самые нужные конструкции без примеров) — чтобы прям как “карманная карта команд”?