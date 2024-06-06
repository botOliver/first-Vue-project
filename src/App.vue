<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import LeftColumn from './components/new components/LeftColumn.vue'
import MainInfromation from './components/new components/MainInfromation.vue'
import { ref } from 'vue'

const inputvalue = ref('')
const checkvalue = ref([])
</script>

<template>
  <div class="body_class">
    <div class="main">
      <form action="" method="get" class="form-example" id="form-example">
        <div id="error_name"></div>

        <div class="form_input">
          <label for="first_name">Имя:*</label>
          <input type="text" placeholder="Иван" id="first_name" style="width: 300px" />
        </div>

        <div id="error_surname"></div>

        <div class="form_input">
          <label for="surname">Фамилия:*</label>
          <input type="text" placeholder="Иванов" id="surname" style="width: 300px" />
        </div>

        <div class="form_input">
          <label for="email">Email:</label>
          <input type="email" placeholder="i.ivanov@mail.ru" id="email" style="width: 300px" />
        </div>

        <div id="error_phone"></div>

        <div class="form_input">
          <label for="phone">Телефон:*</label>
          <input
            type="tel"
            placeholder="+7 000 000-00-00"
            id="phone"
            maxlength="21"
            style="width: 300px"
          />
        </div>

        <span class="characteristics"><strong>Укажите необходимые характеристики:</strong></span>

        <div class="gearbox_type">
          КПП:
          <input type="radio" id="id1" name="kpp" value="id_1" checked />
          <label for="id1">Механическая</label>

          <input type="radio" id="id2" name="kpp" value="id_2" />
          <label for="id2">Автоматическая</label>
        </div>

        <div class="list_values">
          <label for="power">Мощность</label>
          <select id="power" style="width: 300px">
            <option value="poni_1">1 пони</option>
            <option value="poni_4" selected>4 пони</option>
            <option value="poni_125">125 пони</option>
            <option value="max_poni_500">500 пони</option>
          </select>
        </div>

        <div class="note">
          <label for="message">Примечание:</label>
          <textarea
            name="comment"
            placeholder="Расскажите обо всём, что для вас важно"
            id="message"
            style="width: 300px; resize: none"
          ></textarea>
        </div>

        <div class="checkbox">
          <input type="checkbox" />Соглашаюсь на уведомления по указанному email
        </div>

        <button type="submit" class="btn">Отправить</button>

        <div id="error_submit"></div>
      </form>

      <LeftColumn />
      <MainInfromation />
    </div>
  </div>
</template>

<style lang="scss">
h1,
h2,
h3,
h4,
h5,
h6 {
  font-size: 25px;
  line-height: 30.5px;
}

.body_class {
  display: flex;
  box-sizing: border-box;
  justify-content: center;
  font-family: 'Avenir Next'; /* ШРИФТ ПОМЕНЯТЬ! */
  font-size: 22px;
  line-height: 27px;
}

.main {
  display: flex;
  max-width: 1600px;
  padding: 10px;
}

/*! normalize.css v8.0.1 | MIT License | github.com/necolas/normalize.css */

/* Document
   ========================================================================== */

/**
 * 1. Correct the line height in all browsers.
 * 2. Prevent adjustments of font size after orientation changes in iOS.
 */

html {
  line-height: 1.15; /* 1 */
  -webkit-text-size-adjust: 100%; /* 2 */
}

/* Sections
   ========================================================================== */

/**
 * Remove the margin in all browsers.
 */

body {
  margin: 0;
  box-sizing: border-box;
}

/**
 * Render the `main` element consistently in IE.
 */

main {
  display: block;
  box-sizing: border-box;
}

/**
 * Correct the font size and margin on `h1` elements within `section` and
 * `article` contexts in Chrome, Firefox, and Safari.
 */

h1 {
  font-size: 2em;
  margin: 0.67em 0;
  box-sizing: border-box;
}

/* Grouping content
   ========================================================================== */

/**
 * 1. Add the correct box sizing in Firefox.
 * 2. Show the overflow in Edge and IE.
 */

hr {
  box-sizing: content-box; /* 1 */
  height: 0; /* 1 */
  overflow: visible; /* 2 */
}

/**
 * 1. Correct the inheritance and scaling of font size in all browsers.
 * 2. Correct the odd `em` font sizing in all browsers.
 */

pre {
  font-family: monospace, monospace; /* 1 */
  font-size: 1em; /* 2 */
}

/* Text-level semantics
   ========================================================================== */

/**
 * Remove the gray background on active links in IE 10.
 */

a {
  background-color: transparent;
}

/**
 * 1. Remove the bottom border in Chrome 57-
 * 2. Add the correct text decoration in Chrome, Edge, IE, Opera, and Safari.
 */

abbr[title] {
  border-bottom: none; /* 1 */
  text-decoration: underline; /* 2 */
  text-decoration: underline dotted; /* 2 */
}

/**
 * Add the correct font weight in Chrome, Edge, and Safari.
 */

b,
strong {
  font-weight: bolder;
}

/**
 * 1. Correct the inheritance and scaling of font size in all browsers.
 * 2. Correct the odd `em` font sizing in all browsers.
 */

code,
kbd,
samp {
  font-family: monospace, monospace; /* 1 */
  font-size: 1em; /* 2 */
}

/**
 * Add the correct font size in all browsers.
 */

small {
  font-size: 80%;
}

/**
 * Prevent `sub` and `sup` elements from affecting the line height in
 * all browsers.
 */

sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sub {
  bottom: -0.25em;
}

sup {
  top: -0.5em;
}

/* Embedded content
   ========================================================================== */

/**
 * Remove the border on images inside links in IE 10.
 */

img {
  border-style: none;
}

/* Forms
   ========================================================================== */

/**
 * 1. Change the font styles in all browsers.
 * 2. Remove the margin in Firefox and Safari.
 */

button,
input,
optgroup,
select,
textarea {
  font-family: inherit; /* 1 */
  font-size: 100%; /* 1 */
  line-height: 1.15; /* 1 */
  margin: 0; /* 2 */
  box-sizing: border-box;
}

/**
 * Show the overflow in IE.
 * 1. Show the overflow in Edge.
 */

button,
input {
  /* 1 */
  overflow: visible;
}

/**
 * Remove the inheritance of text transform in Edge, Firefox, and IE.
 * 1. Remove the inheritance of text transform in Firefox.
 */

button,
select {
  /* 1 */
  text-transform: none;
}

/**
 * Correct the inability to style clickable types in iOS and Safari.
 */

button,
[type='button'],
[type='reset'],
[type='submit'] {
  -webkit-appearance: button;
}

/**
 * Remove the inner border and padding in Firefox.
 */

button::-moz-focus-inner,
[type='button']::-moz-focus-inner,
[type='reset']::-moz-focus-inner,
[type='submit']::-moz-focus-inner {
  border-style: none;
  padding: 0;
}

/**
 * Restore the focus styles unset by the previous rule.
 */

button:-moz-focusring,
[type='button']:-moz-focusring,
[type='reset']:-moz-focusring,
[type='submit']:-moz-focusring {
  outline: 1px dotted ButtonText;
}

/**
 * Correct the padding in Firefox.
 */

fieldset {
  padding: 0.35em 0.75em 0.625em;
}

/**
 * 1. Correct the text wrapping in Edge and IE.
 * 2. Correct the color inheritance from `fieldset` elements in IE.
 * 3. Remove the padding so developers are not caught out when they zero out
 *    `fieldset` elements in all browsers.
 */

legend {
  box-sizing: border-box; /* 1 */
  color: inherit; /* 2 */
  display: table; /* 1 */
  max-width: 100%; /* 1 */
  padding: 0; /* 3 */
  white-space: normal; /* 1 */
}

/**
 * Add the correct vertical alignment in Chrome, Firefox, and Opera.
 */

progress {
  vertical-align: baseline;
}

/**
 * Remove the default vertical scrollbar in IE 10+.
 */

textarea {
  overflow: auto;
}

/**
 * 1. Add the correct box sizing in IE 10.
 * 2. Remove the padding in IE 10.
 */

[type='checkbox'],
[type='radio'] {
  box-sizing: border-box; /* 1 */
  padding: 0; /* 2 */
}

/**
 * Correct the cursor style of increment and decrement buttons in Chrome.
 */

[type='number']::-webkit-inner-spin-button,
[type='number']::-webkit-outer-spin-button {
  height: auto;
}

/**
 * 1. Correct the odd appearance in Chrome and Safari.
 * 2. Correct the outline style in Safari.
 */

[type='search'] {
  -webkit-appearance: textfield; /* 1 */
  outline-offset: -2px; /* 2 */
}

/**
 * Remove the inner padding in Chrome and Safari on macOS.
 */

[type='search']::-webkit-search-decoration {
  -webkit-appearance: none;
}

/**
 * 1. Correct the inability to style clickable types in iOS and Safari.
 * 2. Change font properties to `inherit` in Safari.
 */

::-webkit-file-upload-button {
  -webkit-appearance: button; /* 1 */
  font: inherit; /* 2 */
}

/* Interactive
   ========================================================================== */

/*
 * Add the correct display in Edge, IE 10+, and Firefox.
 */

details {
  display: block;
}

/*
 * Add the correct display in all browsers.
 */

summary {
  display: list-item;
}

/* Misc
   ========================================================================== */

/**
 * Add the correct display in IE 10+.
 */

template {
  display: none;
}

/**
 * Add the correct display in IE 10.
 */

[hidden] {
  display: none;
}

/* custom */

h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0;
  padding: 0;
}

ul,
li {
  padding: 0;
  margin: 0;
}

li {
  list-style-type: none;
}
</style>
