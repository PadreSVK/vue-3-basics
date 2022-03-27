<template>
    <span>
        <input id="ck" type="checkbox" v-model="checked" />
        <label for="ck">Checked</label>
        <input id="ck2" type="checkbox" v-model="checked2" />
        <label for="ck2">Checked2</label>

        <br />

        <button @click="addData" v-if="!dataIsLoaded">Load data</button>

        <span v-if="dataIsLoaded">
            <ItemA></ItemA>
            <ItemB></ItemB>
        </span>
        <Loading v-else />
    </span>
</template>

<script setup lang="ts">
import { reactive, ref } from 'vue';
import ItemA from './ItemA.vue';
import ItemB from './ItemB.vue';
import Loading from './Loading.vue';

//Alternative to Task.Delay() from .NET
function delay<T>(t : number, v? : T) : Promise<T> {
    return new Promise(function (resolve) {
        setTimeout(resolve.bind(null, v), t)
    });
}



const complexObject = reactive({})
const dataIsLoaded = ref(false)

async function addData() {
    await delay(2000)
    complexObject.test = "asdasd 📅 🥔🥔🥔🥔"
    dataIsLoaded.value = true
}

const checked = ref(true)
const checked2 = ref(true)

</script>

