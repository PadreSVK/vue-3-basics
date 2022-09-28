<script>
import { ref, onMounted } from 'vue'

export default {
    setup() {
        const count = ref(0)

        function increment() {
            count.value++
        }

        // lifecycle hooks
        onMounted(() => {
            console.log(`The initial count is ${count.value}.`)
        })
        // don't forget to expose the function as well.
        return {
            count,
            increment
        }
    }
}
</script>

<template>
    <button @click="increment">Count is: {{ count }}</button>
</template>