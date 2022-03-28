<template>
    <div class="center">
        <input type="checkbox" v-model="treeView" />
        <label for="style">Tree View</label>
        <TreeView v-if="treeView" />
    </div>
</template>

<script setup lang="ts">
import TreeView from './TreeView/TreeView.vue';
import { ref } from 'vue';
const treeView = ref(false)
</script>
