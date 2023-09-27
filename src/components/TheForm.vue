<script setup>

import {ref} from "vue";

const input1 = ref("")
const input2 = ref("")
const input3 = ref("")
const input4 = ref("")

const emit = defineEmits(['sendFormData'])

const sendFormData = () => {
  const formData = {
    inputValue1: input1.value,
    inputValue2: input2.value,
    inputValue3: input3.value,
    inputValue4: input4.value,
  }
  emit("sendFormData", formData)
  input1.value = ""
  input2.value = ""
  input3.value = ""
  input4.value = ""
}

</script>

<template>
  <h1>Form</h1>
  <form @submit.prevent="sendFormData">
    <p><input type="text" v-model="input1"></p>
    <p><input type="text" v-model="input2"></p>
    <p><input type="text" v-model="input3"></p>
    <p><input type="text" v-model="input4"></p>
    <button type="submit">Отправить</button>
  </form>
</template>

<style scoped>

</style>