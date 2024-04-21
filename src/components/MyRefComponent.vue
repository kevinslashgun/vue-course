<script setup>
import { ref, reactive } from 'vue'
let count = ref(0)
let username = ref('')
let usersList = ref(['John', 'Doe', 'Jane', 'Smith'])
let userInfo = ref({ name: 'John', age: 25, location: 'USA', isMarried: false })
let friends = reactive([ref('John'), ref('Doe'), ref('Jane'), ref('Smith')])
</script>

<template>
    <h1>Count: {{ count }}</h1>
    <button @click="count++">Increment</button>
    <button @click="count--">Decrement</button>

    <h1>Username: {{ username }}</h1>
    <button @click="username = 'John'">Add User</button>

    <h1>Users List: {{ usersList }}</h1>
    <button @click="usersList.push('Doe')">Add User</button>

    <h1>User Info</h1>
    <p>Name: {{ userInfo.name }}</p>
    <p>Age: {{ userInfo.age }}</p>
    <p>Location: {{ userInfo.location }}</p>
    <p>Married: {{ userInfo.isMarried }}</p>
    <button @click="userInfo.isMarried = !userInfo.isMarried">Toggle Married</button>

    <h1>Friends List</h1>
    <ul>
        <li v-for="friend in friends" :key="friend">{{ friend }}</li>
    </ul>
    <button @click="friends.forEach(friend => friend.value = '💛')">Hand Shake</button>
</template>