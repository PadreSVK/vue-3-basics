<template>
    <h1>v-show</h1>
    <button @click="addData" v-if="!dataIsLoaded">Load data</button>

    <span v-show="dataIsLoaded">
        <ItemA></ItemA>
        <ItemB></ItemB>
    </span>
    <Loading v-show="!dataIsLoaded" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import ItemA from './ItemA.vue';
import ItemB from './ItemB.vue';
import Loading from './Loading.vue';

//Alternative to Task.Delay() from .NET
function delay<T>(t: number, v?: T): Promise<T> {
    return new Promise(function (resolve) {
        setTimeout(v ? resolve.bind(null, v) : resolve.bind(null), t)
    });
}

const dataIsLoaded = ref(false)
async function addData() {
    await delay(2000)
    dataIsLoaded.value = true
}

</script>

