<template>
    <h3>Complex property</h3>
    <div>{{ todo.description }}</div>
    <div>{{ other }}</div>
    
    <!-- npm run build error => not existing member asdas on type string -->
    <!-- <div>{{ other.asdas }}</div> -->
</template>

<script setup lang="ts">
import type { PropType } from 'vue';
import type { TodoItem } from './Models';

// //runtime based declaration
// defineProps({
//     todo:{
//         type:Object, // we are not able to use type TodoItem => it expect object/value not TS type 
//         required: true
//     },
//     other:{
//         type: String
//     }
// })


// //interface based declaration
// interface Props {
//     todo: TodoItem
//     other?: string
// }
// defineProps<Props>()

// //type based declaration
defineProps<{
    todo: TodoItem
    other?: string
}>()


defineProps({
    value: {
        type: null as unknown as PropType<string | null>,
        default: null,
        required: false
    }
})

</script>

<style scoped>
</style>