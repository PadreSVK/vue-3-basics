<template>
    <h1>Emit events</h1>
    <button @click="emitWithoutPayload">Emit without payload</button>
    <button @click="emitWithPayload">Emit with payload</button>

    <!-- $event => native Event in handler -->
    <button @click="logNativeEvent">log native Event (implicit argument)</button>
    <button @click="logNativeEvent($event)">log native Event (explicit argument)</button>
</template>

<script setup lang="ts">

const emit = defineEmits(["btn-clicked", "btn-clicked-payload"])

function emitWithoutPayload() {
    console.log("emiting event....")
    emit('btn-clicked')
}
function emitWithPayload() {
    console.log("emiting event....")
    emit('btn-clicked-payload', { test: "Fero", age: 999 })
}

function logNativeEvent(event: Event) {
    console.log(event)
}

</script>

