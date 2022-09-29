<template>
    <div>
        <span>Count: {{store.count}}</span>
        <button @click="store.increment()">Increase Value from random component 2</button>
    </div>
</template>

<script setup lang="ts">
import { useCounterStore } from './store';
const store = useCounterStore()

</script>