<template>
    <h1>Simple event handlers (native DOM events)</h1>
    <!-- add event handler for click event (any element) -->
    <h1 @click="clickedHeader">Item A - click on me</h1>
    <!-- add event handler for click event on button -->
    <button @click="clicked">Click</button>
</template>

<script setup lang="ts">

function clicked() {
    console.log("clicked in Item A on Click button")
}

function clickedHeader() {
    console.log("clicked on Item A header")
}

</script>

