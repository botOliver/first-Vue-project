<script setup lang="ts">
import { ref } from 'vue'

const surName = ref('')
const errorMessageSurName = ref(false)
const isInvalidSurName = ref(false)

const fnBlurSurname = () => {
  if (surName.value === '') {
    console.log('проверка1')
    errorMessageSurName.value = true
    isInvalidSurName.value = true
  }
}

const fnFocusSurName = () => {
  if (isInvalidSurName.value === true) {
    isInvalidSurName.value = false
    errorMessageSurName.value = false
  }
}
</script>

<template>
  <div id="error_surname" v-if="errorMessageSurName" class="red-text">
    Пожалуйста, введите правильную фамилию
  </div>

  <div class="form_input">
    <label for="surname">Фамилия:*</label>
    <input
      v-model="surName"
      :class="{ invalid: isInvalidSurName }"
      @blur="fnBlurSurname"
      @focus="fnFocusSurName"
      type="text"
      placeholder="Иванов"
      id="surname"
      style="width: 300px"
    />
  </div>
</template>

<style scoped></style>
