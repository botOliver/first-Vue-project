<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <section class="left-column">
    <img
      class="left-column__image"
      src="/src/assets/photo_2024-02-24_21-03-13 — копия.jpg"
      alt="моя фотография"
    />

    <h2 class="left-column_header">Пак Герман</h2>

    <h2 class="left-column__about">Junior frontend developer</h2>

    <article class="left-column__information">
      <ul class="column__information-list">
        <li class="left-column__information-item"><span>Возраст:</span><span>26</span></li>
        <li class="left-column__information-item">
          <span>Профессия:</span><span>Frontend developer</span>
        </li>
        <li class="left-column__information-item">
          <span>Телефон:</span><span>+9 (999) 000-00-00</span>
        </li>
        <li class="left-column__information-item">
          <span>Город:</span><span>Санкт-Петербург</span>
        </li>
      </ul>
    </article>

    <article class="left-column__skills">
      <ul class="left-column__skills-list">
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
        <li>TypeScript</li>
        <li>Vue2</li>
        <li>Vue3</li>
        <li>Vite</li>
        <li>NPM</li>
        <li>GIT</li>
        <li>Figma</li>
        <li>Docker</li>
      </ul>
    </article>

    <article class="left-column__contacts">
      <a href="https://t.me/veryangryhuman" target="_blank" class="left-column__social">
        <img src="/src/assets/telegram-icon.png" alt="Иконка телеграма" />
        <span class="Telegram">Telegram</span>
      </a>

      <a href="https://vk.com/asdxqwerty" target="_blank" class="left-column__social">
        <img src="/src/assets/vk-icon.png" alt="Иконка ВКонтакте" />
        <span>ВКонтакте</span>
      </a>

      <a href="mailto:botoliver556@gmail.com" target="_blank" class="left-column__social">
        <img src="/src/assets/gmail-icon.png" alt="Иконка Gmail" />
        <span>Gmail</span>
      </a>
    </article>
  </section>
</template>

<style lang="scss" scoped>
.left-column {
  min-width: 360px;
  max-width: 469px;
  max-height: 950px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #f7f7f7;
  box-sizing: border-box;
  padding: 20px 10px 20px;
  margin: 25px 35px 0 1px;
  gap: 30px;

  &__image {
    display: block;
    width: 82%;
    border-radius: 50%;
    filter: grayscale(100%);
    box-shadow: 0px 7px 11px 0px #74747480;
  }

  &_header {
    display: none;
  }

  &__information {
    max-width: 349px;
    width: 95%;
  }
}

.left-column__information {
  max-width: 349px;
  width: 95%;
}

.left-column__information-item {
  display: flex;
  justify-content: space-between;
}

.left-column__skills-list {
  max-width: 349px;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
}

.left-column__skills-list > li {
  background-color: #7b7b7b;
  color: #ffffff;
  padding: 5px;
  font-size: 18px;
}

.left-column__contacts {
  display: flex;
  max-width: 349px;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
}

.left-column__social {
  display: flex;
  align-items: center;
  max-width: 150px;
  max-height: 45px;
  text-decoration: none;
  color: black;
}
.left-column__social > img {
  max-width: 30px;
  max-height: 30px;
  margin-right: 5px;
}

.telegram {
  color: #24a4ec;
}
</style>
