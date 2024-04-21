<script setup>
import { ref, computed } from 'vue'
const number = ref(5)
const squaredNumber = computed(() => number.value * number.value)

const firstName = ref('John')
const lastName = ref('Doe')

const fullName = computed(() => `${firstName.value} ${lastName.value}`)

const counter = ref(0)
const squaredCounter = computed(() => counter.value ** 2)
</script>

<template>
    <h1>Original Number: {{ number }}</h1>
    <h1>Squared Number: {{ squaredNumber }}</h1>
    <h1>Full Name: {{ fullName }}</h1>
    <h1>Counter: {{ counter }}</h1>
    <h1>Squared Counter: {{ squaredCounter }}</h1>
    <button @click="counter++">Increment Counter</button>
</template>