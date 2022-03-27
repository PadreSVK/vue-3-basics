<template>
    <div></div>
    <ListItem
        v-for="item in items"
        :key="item.id"
        :marker="item.marker"
        :description="item.description"
    />
</template>

<script setup lang="ts">


import ListItem from './ListItem.vue';

defineProps({
    items: {
        default: [{ id: 1234, marker: "🎈", description: "Lorem Ipsum" }]

    }
})

</script>
