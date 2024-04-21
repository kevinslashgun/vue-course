<script setup>
import { ref } from 'vue'
const name = ref('')
const email = ref('')
</script>

<template>
    <form @submit.prevent="$emit('userInfo', name, email)">
        <input type="text" placeholder="Name" v-model="name" />
        <input type="email" placeholder="Email" v-model="email" />
        <button>Submit</button>
    </form>
</template>