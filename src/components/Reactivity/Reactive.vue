<template>
    <h1>Reactive</h1>
    {{ complexReactiveProperty }}
    <input type="text" v-model="complexReactiveProperty.name" />
    <button @click="changeName">Change name of object</button>
</template>

<script setup lang="ts">
import { reactive } from 'vue';

//make object reactive via js Proxy object => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy
const complexReactiveProperty = reactive({ name: "Patrik", age: 15 })

function changeName() {
    //direct change of property
    complexReactiveProperty.name = "Fero"
}

</script>

<style scoped>
</style>