<template>
    <div :class="classes">
        <h1>Hellou from component</h1>

        <input type="checkbox" v-model="classes.center" id="isCenter" />
        <label for="isCenter">Center</label>
        <input type="checkbox" v-model="classes['static-class']" id="isStatic" />
        <label for="isStatic">isStatic</label>

        <input type="text" v-model="myStyleObject.color" />
        <input type="text" v-model="myStyleObject.width" />
    </div>
</template>

<script setup lang="ts">

import { reactive } from "vue";

const myStyleObject = reactive({
    color: "red",
    width: "50%"
})

const classes = reactive({
    center: true,
    "static-class": true
})

</script>

<style scoped>
.center {
    margin: auto;
    width: v-bind("myStyleObject.width");
    padding: 10px;
    border: 3px solid v-bind("myStyleObject.color");
}

.static-class {
    color: black;
}
</style>