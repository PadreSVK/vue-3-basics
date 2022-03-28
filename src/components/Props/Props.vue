<template>
    <h3>Props</h3>
    <input type="text" v-model="name"/>
    <Simple :name="name" />
    <Complex :name="name" />
    

</template>

<script setup lang="ts">
import { ref } from "vue";
import TwoWayDataBinding from "../TwoWayDataBinding/TwoWayDataBinding.vue";
import Simple from "./Simple.vue";

const name = ref("")

</script>

<style scoped>
</style>