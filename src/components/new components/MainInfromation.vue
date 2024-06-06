<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <section class="main-information">
    <header class="main-information__header">
      <h1>Пак Герман</h1>
    </header>

    <h2 class="main-information__subheader">Обо мне:</h2>
    <p class="main-information__about">
      Я приверженец активного и позитивного образа жизни. Всегда стараюсь построить рабочий процесс
      так, чтобы люди, работающие со мной в команде, чувствовали себя комфортно и проявляли интерес
      к проекту. Всегда готов искренне помочь или выслушать. Активно участвую в корпоративной жизни
      и мероприятиях. В свободное время увлекаюсь музыкой, коллекционированием лего, кинематографом.
    </p>

    <div class="skills__wrapper">
      <!-- ТУТ СКИЛЛЫ И НАВЫКИ -->
      <div class="main-information__skills">
        <div class="main-information__job">
          <h3>Медицинский брат</h3>
          <div class="main-information__job-date">Апрель 2019 - Октябрь 2023</div>
          <p>ГБУЗ Ленинградская областная клиническая больница, Санкт-Петербург.</p>

          <div class="main-information__responsibilities">
            <div class="main-information__point"></div>
            <span>Доврачебная медицинская помощь</span>
          </div>

          <div class="main-information__responsibilities">
            <div class="main-information__point"></div>
            <span>Руководство младшим мед. персоналом</span>
          </div>

          <div class="main-information__responsibilities">
            <div class="main-information__point"></div>
            <span>Организация ухода за больным</span>
          </div>
        </div>
      </div>

      <div class="main-information__progress">
        <div class="main-information__softs">
          <h3>Навыки:</h3>
          <div class="main-information__personality">
            <div class="main-information-levels">
              <div>Elementary</div>
              <div>Advanced</div>
            </div>
            <div class="main-information__personality-line">
              <div class="main-information__personality-point english"></div>
            </div>
          </div>

          <div class="main-information__personality">
            <div class="main-information-levels">
              <div>Интроверт</div>
              <div>Экстраверт</div>
            </div>
            <div class="main-information__personality-line">
              <div class="main-information__personality-point psychotype"></div>
            </div>
          </div>

          <div class="main-information__personality">
            <div class="main-information-levels">
              <div>Рассеяный</div>
              <div>Организованный</div>
            </div>
            <div class="main-information__personality-line">
              <div class="main-information__personality-point organization"></div>
            </div>
          </div>

          <div class="main-information__personality">
            <div class="main-information-levels">
              <div>Инертный</div>
              <div>Любознательный</div>
            </div>
            <div class="main-information__personality-line">
              <div class="main-information__personality-point educability"></div>
            </div>
          </div>

          <div class="main-information__personality">
            <div class="main-information-levels">
              <div>Нервный</div>
              <div>Стрессоустойчивый</div>
            </div>
            <div class="main-information__personality-line">
              <div class="main-information__personality-point stress"></div>
            </div>
          </div>
        </div>

        <div class="main-information__education">
          <h3>Образование:</h3>
          <div class="main-information__university">
            Высшее: Военно-медицинская академия им. С. М. Кирова. Лечебный факультет 2021г.
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.skills__wrapper {
  display: flex;
  margin-top: 22px;
  gap: 100px;
}

.main-information {
  box-sizing: border-box;
  margin-top: 62px;
  max-width: 961px;
  min-width: 100%;
}

.main-information__header > h1 {
  font-size: 97px;
  line-height: 118px;
}

.main-information__about {
  margin-top: 22px;
  text-indent: 20px;
}

.main-information__skills {
  display: flex;
  justify-content: space-between;
}

.main-information__job,
.main-information__progress {
  max-width: 440px;
}

.main-information__job > h3,
.main-information__softs > h3,
.main-information__education > h3 {
  margin-bottom: 22px;
}

.main-information__responsibilities {
  display: flex;
}

.main-information__point {
  margin: 7px 5px 0 0;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #7b7b7b;
}

.main-information__progress,
.main-information__softs,
.main-information__personality {
  display: flex;
  flex-direction: column;
}

.main-information__personality {
  gap: 5px;
}

.main-information-levels {
  display: flex;
  justify-content: space-between;
}

.main-information__personality-line {
  position: relative;
  height: 3px;
  background-color: #d2d2d2;
  margin: 5px 7px;
}

.main-information__personality-point {
  position: absolute;
  bottom: -8px;
  width: 16px;
  height: 16px;
  background-color: #7b7b7b;
  border: 2px solid #ffffff;
  border-radius: 50%;
}

.english {
  margin-left: 59%;
}

.psychotype {
  margin-left: 65%;
}

.organization {
  margin-left: 76%;
}

.educability {
  margin-left: 70%;
}

.stress {
  margin-left: 80%;
}

.main-information__education {
  margin-top: 30px;
}
</style>
