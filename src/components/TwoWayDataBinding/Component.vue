<template>
    <input type="text" :value="props.name" @change="update(($event.target as any).value)" />
</template>

<script setup lang="ts">
const props = defineProps({
    name: {
        type: String,
    }
})

const emit = defineEmits(["update:name"])
function update(value: string) {
    emit('update:name', value)
}

</script>

<style scoped>
</style>