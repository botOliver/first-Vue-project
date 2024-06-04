<script setup lang="ts">
import NameInput from './NameInput/NameInput.vue';
import { reactive, ref } from 'vue'

const isInvalidName = ref(false)

const fieldsOfForm = reactive({
  firstName: {
    value: '',
    error: false
  }
})



const checkField = (fieldName: string, value: boolean = false): void => {
  fieldsOfForm[fieldName].error = !value;
  isInvalidName.value = fieldsOfForm[fieldName].error
}

const resetError = (fieldName: string): void => {
  fieldsOfForm[fieldName].error = false
  isInvalidName.value = false
}

// Когда мы используем квадратные скобки для доступа к свойству объекта, 
// имя свойства обычно указывается в кавычках, чтобы JavaScript понимал, 
// что это имя свойства, а не переменная или что-то ещё.
</script>

<template>


  <div id="error_name" v-if="fieldsOfForm.firstName.error" class="red-text">
    Пожалуйста, введите правильное имя
  </div>

  <div class="form_input">
    <label for="first_name">Имя:*</label>
    <input
      v-model="fieldsOfForm.firstName.value"
      @blur="checkField('firstName', fieldsOfForm.firstName.value)"
      @focus="resetError('firstName')"
      @input="resetError('firstName')"
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
