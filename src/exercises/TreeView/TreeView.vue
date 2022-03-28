<template>
    <ul>
        <TreeViewItem class="item" :model="treeData" />
    </ul>
</template>

<script setup lang="ts">
import { ref } from "vue";
import TreeViewItem from "./TreeViewItem.vue";

const treeData = ref({
    name: 'My Tree',
    children: [
        { name: 'hello' },
        { name: 'world' },
        {
            name: 'child folder',
            children: [
                {
                    name: 'child folder',
                    children: [{ name: 'hello' }, { name: 'world' }]
                },
                { name: 'hello' },
                { name: 'world' },
                {
                    name: 'child folder',
                    children: [{ name: 'hello' }, { name: 'world' }]
                }
            ]
        }
    ]
})
</script>