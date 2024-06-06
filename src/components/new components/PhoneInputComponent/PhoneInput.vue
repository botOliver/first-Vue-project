<script setup lang="ts">
import { ref, reactive } from 'vue'


const phoneError = ref(false)


const fieldsOfForm = reactive({
  phoneNumber:{
    value: '',
    error: false
  }
})

const checkField = (fieldName: string, value:boolean ):void => {
  fieldsOfForm[fieldName].error = !value
    phoneError.value = fieldsOfForm[fieldName].error
  console.log(phoneError.value)
}


const errorMessage = (fieldName:string):void=>{
  fieldsOfForm.phoneNumber.error = false
  console.log(fieldsOfForm.phoneNumber.error)
}

</script>

<template>
  <div id="error_phone" v-if="fieldsOfForm.phoneNumber.error" class="red-text">
    Пожалуйста, введите правильный номер телефона
  </div>

  <div class="form_input">
    <label for="phone">Телефон:*</label>
    <input
      v-model="fieldsOfForm.phoneNumber.value"
      @blur="checkField('phoneNumber', fieldsOfForm.phoneNumber.value)"
      @focus="errorMessage('phoneNumber')"
      @input="errorMessage('phoneNumber')"
      :class="{invalid:phoneError}"
      type="tel"
      placeholder="+7 000 000-00-00"
      id="phone"
      maxlength="21"
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
}
</style>
