<template>
    <div class="center">
        <!-- <MyStyleComponent/> -->
        <!-- <Conditions/> -->
        <Watch />
    </div>
</template>

<script setup lang="ts">
import MyStyleComponent from './components/Style/MyStyleComponent.vue';
import Conditions from './components/Conditions/Conditions.vue';
import Watch from './components/Watch/Watch.vue';

</script>

<style>
.center {
    margin: auto;
    width: 50%;
    padding: 10px;
    border: 3px solid green;
}
</style>
