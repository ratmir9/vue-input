<script setup>
import TheForm from "./components/TheForm.vue";


const printFormData = (formData) => {
  console.group("Form Data")
  for (const key in formData){
    console.log(`${key} : ${formData[key]}`)
  }
  console.groupEnd()
}


</script>

<template>
  <TheForm @sendFormData="printFormData"/>
</template>