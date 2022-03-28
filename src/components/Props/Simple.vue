<template>
    <h3>Simple property</h3>
    <span>{{ name }}</span>
</template>

<script setup lang="ts">
defineProps(["name"])

//alternative syntax = for script access
// const props = defineProps(["name"])
// const name = props.name // in script access
</script>