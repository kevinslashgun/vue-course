<script setup>
const isUserLoggedIn = false;
</script>

<template>
    <div>
        <h2 v-if="isUserLoggedIn">Welcome, User!</h2>
        <h2 v-else>Welcome, Guest!</h2>
        <p v-show="isUserLoggedIn"> This paragraph is visible if you are logged.</p>
    </div>
</template>