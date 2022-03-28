<template>
    <h1>Events</h1>
    <SimpleEvents />
    <Emit @btn-clicked="btnClicked" @btn-clicked-payload="btnClickedPayload" />
    <Complex @btn-clicked="btnClicked" @btn-clicked-payload="btnClickedPayload" />
</template>

<script setup lang="ts">

import SimpleEvents from "./SimpleEvents.vue";
import Emit from "./Emit.vue";
import Complex from "./Complex.vue";

function btnClicked() {
    console.log("btnClicked => without payload");
}

// without deconstruct
// function btnClickedPayload(value : { test: string, age: number} ) {

//with deconstruct
function btnClickedPayload({ age, test }: { test: string, age: number }) {
    console.log("btnClickedPayload => with payload");
    console.log({ test })
    console.log({ age })
}

</script>
