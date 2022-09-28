<template>
    <!-- OneWayDataBinding -->
    <Component :name="name" />

    <!-- TwoWayDataBinding -->
    <Component :name="name"  @update:name="name = $event"/>

    <!-- simplified -->
    <Component v-model:name="name"/>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Component from "./Component.vue";

const name = ref("")

</script>
