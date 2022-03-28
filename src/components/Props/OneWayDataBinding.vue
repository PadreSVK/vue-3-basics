<template>
    <h3>OneWayDataBinding</h3>
    <span>{{ name }}</span>
</template>

<script setup lang="ts">
defineProps(["name"])

//alternative syntax = for script access
// const props = defineProps(["name"])
// access via
// const name = props.name
</script>