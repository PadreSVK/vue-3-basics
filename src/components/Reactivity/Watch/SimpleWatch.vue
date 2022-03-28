<template>
    <h1>SimpleWatch</h1>
    {{ todo }}
    <div class="col">
        <div class="row">
            Id:
            <input type="text" v-model="todo.id" />
        </div>
        <div class="row">
            Desciption:
            <textarea v-model="todo.description"></textarea>
        </div>
    </div>
</template>

<script setup lang="ts">
import { reactive, watch } from 'vue';

const todo = reactive({
    id: "3f99d915-2348-4cb1-a893-a43a1eee4ad2",
    description: "Renard",
    completed: new Date(),
    done: true,
})

// deep watch => update on any change on todo
watch(todo, updatedTodo => {
    console.log("watch(todo, updatedTodo => {");
    console.log(updatedTodo)
})

// watch => update on todo.description (+ old value is avaliable)
watch(() => todo.description, (newVal, oldVal) => {
    console.log("watch(() => todo.description, (newVal, oldVal) => {");
    console.log({ newVal, oldVal })
})


</script>

<style scoped>
.col {
    display: flex;
    flex-direction: column;
}
.row {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
</style>