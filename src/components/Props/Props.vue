<template>
    <h3>Props</h3>
    <input type="text" v-model="name"/>
    <OneWayDataBinding :name="name" />
    
    <!-- OneWayDataBinding -->
    <!-- <TwoWayDataBinding :name="name" /> -->

    <!-- TwoWayDataBinding -->
    <TwoWayDataBinding :name="name"  @update:name="name = $event"/>
    <!-- simplified -->
    <TwoWayDataBinding v-model:name="name"/>
</template>

<script setup lang="ts">
import { ref } from "vue";
import TwoWayDataBinding from "./TwoWayDataBinding.vue";
import OneWayDataBinding from "./OneWayDataBinding.vue";

const name = ref("")

</script>

<style scoped>
</style>