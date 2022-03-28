<template>
    <h1>Computed</h1>
    {{ computedProperty }}
    <input type="text" v-model="complexReactiveProperty.name" />
</template>

<script setup lang="ts">
import { computed, reactive } from 'vue';

const complexReactiveProperty = reactive({ name: "Patrik", age: 15 })

const computedProperty = computed(() => `decoratedName ${complexReactiveProperty.name}: ${complexReactiveProperty.age}`)

</script>

<style scoped>
</style>