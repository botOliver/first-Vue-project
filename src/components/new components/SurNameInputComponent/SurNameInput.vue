<script setup lang="ts">

import { reactive, ref } from 'vue'

const isInvalidSurName = ref(false)



const fieldsOfForm = reactive({
  surName:{
    value: '', 
    error: false
  }
}) 

const resetError = (fieldName:string) :void=>{
  fieldsOfForm[fieldName].error = false
}


const checkField = (fieldName:string, value: boolean = false):void=>{
  fieldsOfForm[fieldName].error = !value
  isInvalidSurName.value = !value
}


</script>

<template>
  <div id="error_surname" v-if="fieldsOfForm.surName.error" class="red-text">
    Пожалуйста, введите правильную фамилию
  </div>

  <div class="form_input">
    <label for="surname">Фамилия:*</label>
    <input
      v-model="fieldsOfForm.surName.value"
      @blur="checkField('surName', fieldsOfForm.surName.value)"
      @focus="resetError('surName')"
      @input="resetError('surName')"
      :class="{ invalid: isInvalidSurName }"
      type="text"
      placeholder="Иванов"
      id="surname"
      style="width: 300px"
    />
  </div>
</template>

<style scoped></style>
