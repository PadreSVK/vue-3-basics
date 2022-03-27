<template>
    <div>
        {{ props.marker }}:
        {{ props.description }}
        <input v-model="props.marker" />
    </div>
</template>

<script setup lang="ts">

const props = defineProps({
    marker: {
        required: true
    },
    description: {
        required: true
    },
})

</script>
