<script setup>
import FormComponent from './components/FormComponent.vue';

const formHandler = (name, email) => {
  console.log(name, email);
}
</script>

<template>
  <h1>Hello</h1>
  <FormComponent @userInfo="formHandler" />
</template>

<style scoped></style>