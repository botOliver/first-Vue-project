<script setup lang="ts">
import { ref } from 'vue'
const firstName = ref('')
const errorMessageName = ref(false)
const isInvalidName = ref(false)

// function handleChange(event: Event) {
//   if ((event.target as HTMLInputElement).value === firstName.value) {
//     console.log((event.target as HTMLInputElement).value)
//   }
// }

const fnBlurName = (parametr: string) => {
  if (parametr === '') {
    console.log('проверка')
    errorMessageName.value = true
    isInvalidName.value = true
  } else {
    console.log('нижняя часть')
    isInvalidName.value = false
    console.log(errorMessageName.value)
    errorMessageName.value = false
  }
}

// const fnBlurName = () => {
//   if (firstName.value === '') {
//     console.log('проверка')
//     errorMessageName.value = true
//     isInvalidName.value = true
//   }
// }

// const fnFocusName = () => {
//   if (isInvalidName.value === true) {
//     isInvalidName.value = false
//     errorMessageName.value = false
//   }
// }

// @change="firstTry"
//       @blur="fnBlurName(firstName)"
//       @focus="fnFocusName"
</script>

<template>
  <div id="error_name" v-if="errorMessageName" class="red-text">
    Пожалуйста, введите правильное имя
  </div>

  <div class="form_input">
    <label for="first_name">Имя:*</label>
    <input
      @blur="fnBlurName(firstName)"
      v-model="firstName"
      :class="{ invalid: isInvalidName }"
      type="text"
      placeholder="Иван"
      id="first_name"
      style="width: 300px"
    />
  </div>
</template>

<style scoped>
.invalid {
  border-color: red;
}

#error_name,
#error_surname,
#error_phone {
  color: red;
  text-align: right;
  font-size: 15px;
  border-color: red;
}
</style>
