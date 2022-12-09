<template>
  <div>
   <Button @click="sayHello" />
   <p :class="toshow"> {{helloWorld()}}</p>
  </div>

</template>

<script setup>
import Button from "./components/Button.vue" ; 
import {ref} from "vue";

function helloWorld(){
  return `Hello World`;
}
const toshow = ref("hidden")

function sayHello() {
    toshow.value === "hidden" ? toshow.value = "show" : toshow.value = "hidden";
    return toshow.value;
}

</script>

<style>
.show{
  display: block;
}
.hidden {
  display: none;
}
</style>
