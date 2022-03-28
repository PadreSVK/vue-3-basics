<template>
    <div class="center">
        <!-- <Reactivity /> -->
        <Conditions />
        <!-- <MyStyleComponent/> -->
        <!-- <Conditions/> -->
        <!-- <Reactivity /> -->
    </div>
</template>

<script setup lang="ts">
import MyStyleComponent from './components/Style/MyStyleComponent.vue';
import Conditions from './components/Conditions/Conditions.vue';
import Reactivity from './components/Reactivity/Reactivity.vue';

</script>

<style>
.center {
    margin: auto;
    width: 50%;
    padding: 10px;
    border: 3px solid green;
}
</style>
