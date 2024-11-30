<template>
    <div>
        <h1>{{ message }}</h1>
        <button @click="changeMessage">change Message</button>
    </div>
</template>

<script setup>
import { ref } from "vue";

const message = ref('Hello, Nuxt with Vue 3!')

const changeMessage = () => {
    message.value = 'Message changed!!'
}
</script>

<style scoped>
h1 {
  color: #42b883;
  text-align: center;
}
button {
  margin-top: 10px;
  padding: 5px 10px;
  font-size: 16px;
  cursor: pointer;
}
</style>