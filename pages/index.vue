<template>
    <div>
        <h1>Hello, World!</h1>
        <HelloWorld/>
    </div>
</template>

<script setup>
import HelloWorld from '~/components/HelloWorld.vue'
</script>

<style>
    /* スタイルの追加例 */
h1 {
  color: #42b883;
  font-family: Arial, sans-serif;
  text-align: center;
}
p {
  text-align: center;
  color: #35495e;
}
</style>