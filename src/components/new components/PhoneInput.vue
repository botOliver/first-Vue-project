<script setup lang="ts">
import { ref, computed } from 'vue'
const isInvalidPhoneNumber = ref(false)
const errorMessagePhoneNumber = ref(false)
const phoneNumber = ref('')

const fnBlurPhoneNumber = () => {
  if (phoneNumber.value === '') {
    errorMessagePhoneNumber.value = true
    isInvalidPhoneNumber.value = true
  }
}

const fnFocusPhoneNumber = () => {
  if (isInvalidPhoneNumber.value === true) {
    isInvalidPhoneNumber.value = false
    errorMessagePhoneNumber.value = false
  }
}
</script>

<template>
  <div id="error_phone" v-if="errorMessagePhoneNumber" class="red-text">
    Пожалуйста, введите правильный номер телефона
  </div>

  <div class="form_input">
    <label for="phone">Телефон:*</label>
    <input
      v-model="phoneNumber"
      :class="{ invalid: isInvalidPhoneNumber }"
      @blur="fnBlurPhoneNumber"
      @focus="fnFocusPhoneNumber"
      type="tel"
      placeholder="+7 000 000-00-00"
      id="phone"
      maxlength="21"
      style="width: 300px"
    />
  </div>
</template>

<style scoped></style>
