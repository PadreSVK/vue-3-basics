<template>
    <h1>Ref</h1>
    <input type="text" v-model="name" />
    <button @click="changeName">Change value of ref</button>
</template>

<script setup lang="ts">
import { ref } from 'vue';

//reactive "value"
const name = ref("Patrik")

function changeName() {
    //direct change only via value property
    name.value = "Fero"
}

</script>

<style scoped>
</style>