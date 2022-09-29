<template>
    <button @click="store.increment()">Increase Value from random component</button>
</template>

<script setup lang="ts">
import { useCounterStore } from './store';
const store = useCounterStore()

</script>

