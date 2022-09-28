<template>
    <div class="center">
        <input type="checkbox" v-model="apistyles" id="apistyles" />
        <label for="apistyles">API Styles</label>
        
        <input type="checkbox" v-model="reactivity" id="reactivity" />
        <label for="reactivity">Reactivity</label>
        
        <input type="checkbox" v-model="conditions" />
        <label for="conditions">Conditions</label>
        
        <input type="checkbox" v-model="props" />
        <label for="props">Props</label>
        
        <input type="checkbox" v-model="events" />
        <label for="events">Events</label>

        <input type="checkbox" v-model="twoWayBinding" />
        <label for="twoWayBinding">Two way data binding</label>
        
        <input type="checkbox" v-model="style" />
        <label for="style">Style</label>
        
        <input type="checkbox" v-model="exercises" />
        <label for="exercises">Exercises</label>

        <APIStyles v-if="apistyles" />
        <Reactivity v-if="reactivity" />
        <Reactivity v-if="reactivity" />
        <Conditions v-if="conditions" />
        <Props v-if="props" />
        <Events v-if="events" />
        <TwoWayDataBinding v-if="twoWayBinding"/>
        <Styles v-if="style" />
        <Exercises v-if="exercises"/>

    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import APIStyles from './components/APIStyles/APIStyles.vue';
import Reactivity from './components/Reactivity/Reactivity.vue';
import Conditions from './components/Conditions/Conditions.vue';
import Props from './components/Props/Props.vue';
import Events from './components/Events/Events.vue';
import TwoWayDataBinding from './components/TwoWayDataBinding/TwoWayDataBinding.vue';
import Styles from './components/Style/Style.vue';
import Exercises from './exercises/Exercises.vue';


const apistyles = ref(false)
const reactivity = ref(false)
const conditions = ref(false)
const props = ref(false)
const events = ref(false)
const style = ref(false)
const twoWayBinding = ref(false)
const exercises = ref(false)

</script>

<style>
.center {
    margin: auto;
    width: 50%;
    padding: 10px;
    border: 3px solid green;
}
</style>
