<template>
    <h1>Events</h1>
    <SimpleEvents />
    <Emit @btn-clicked="btnClicked" @btn-clicked-payload="btnClickedPayload" />
</template>

<script setup lang="ts">

import SimpleEvents from "./SimpleEvents.vue";
import Emit from "./Emit.vue";

function btnClicked() {
    console.log("btnClicked => without payload");
}

function btnClickedPayload(payload: any) {
    console.log("btnClickedPayload => with payload");
    console.log({ payload })
}

</script>
