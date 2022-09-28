<template>
    <h1>Style</h1>
    <div :class="{ center: classes.center }">Some content</div>

    <div :class="classes">
        <input type="checkbox" v-model="classes.center" id="isCenter" />
        <label for="isCenter">Center</label>

        <input type="checkbox" v-model="classes['static-class']" id="isStatic" />
        <label for="isStatic">Is Static</label>

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
<!-- scoped add attribute to every element from template -->
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