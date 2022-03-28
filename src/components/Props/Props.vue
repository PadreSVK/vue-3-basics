<template>
    <h3>Props</h3>
    <input type="text" v-model="name"/>
    <Simple :name="name" />
    <Complex :todo="todo" other="my name is" />
    <Complex :todo="todo" :other="name" />

    <!-- npm run build error => wrong type -->
    <!-- <Complex :todo="todo2" /> -->
</template>

<script setup lang="ts">
import { reactive, ref } from "vue";
import Simple from "./Simple.vue";
import Complex from "./Complex.vue";
import type { TodoItem } from "./Models";


const name = ref("")

const todo2 = reactive({
    id: "3f99d915-2348-4cb1-a893-a43a1eee4ad2",
    description: "Renard",
})

const todo : TodoItem  = reactive({
    id: "3f99d915-2348-4cb1-a893-a43a1eee4ad2",
    description: "Renard",
    completed: new Date(),
    done: true,
})

</script>

<style scoped>
</style>