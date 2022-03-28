<template>
    <div class="center">
        <input type="checkbox" v-model="reactivity" id="reactivity" />
        <label for="reactivity">Reactivity</label>
        <input type="checkbox" v-model="conditions" />
        <label for="conditions">Conditions</label>
        <input type="checkbox" v-model="props" />
        <label for="props">Props</label>
        <input type="checkbox" v-model="events" />
        <label for="events">Events</label>

        <Reactivity v-if="reactivity" />
        <Conditions v-if="conditions" />
        <Props v-if="props" />
        <Events v-if="events" />
        <!-- <MyStyleComponent/> -->
        <!-- <Conditions/> -->

    </div>
</template>

<script setup lang="ts">
import Reactivity from './components/Reactivity/Reactivity.vue';
import Conditions from './components/Conditions/Conditions.vue';
import Props from './components/Props/Props.vue';

import MyStyleComponent from './components/Style/MyStyleComponent.vue';
import { ref } from 'vue';
import Events from './components/Events/Events.vue';

const reactivity = ref(false)
const conditions = ref(false)
const props = ref(false)
const events = ref(false)

</script>

<style>
.center {
    margin: auto;
    width: 50%;
    padding: 10px;
    border: 3px solid green;
}
</style>
