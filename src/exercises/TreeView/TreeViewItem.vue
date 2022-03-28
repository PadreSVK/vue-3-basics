<template>
    <li>
        <div :class="{ bold: isFolder }" @click="toggle">
            <span v-if="isFolder">[{{ expandIcon }}]</span>
            {{ props.model.name }}
        </div>
        <ul v-show="isOpen" v-if="isFolder">
            <!--A component can recursively render itself using its "name" option (inferred from filename if using SFC)-->
            <TreeViewItem class="item" v-for="item in model.children" :model="item" />
        </ul>
    </li>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const props = defineProps({
    model: {
        type: Object,
        required: true
    },
})

const expandIcon = computed(() => isOpen.value ? '➖' : '➕')

const isOpen = ref(false)
const isFolder = computed(() => props.model.children?.length > 0)

function toggle() {
    isOpen.value = !isOpen.value
}
</script>

<style>
.item {
    cursor: pointer;
    line-height: 1.5;
}
.bold {
    font-weight: bold;
}
</style>