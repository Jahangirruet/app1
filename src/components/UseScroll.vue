<template>
  <div>
    <div class="ex1" ref="scrollbox">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
      nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
    </div>
    <div>
      <pre>
      {{ scroll }}
     </pre
      >
    </div>
  </div>
</template>

<script setup>
import ref from "vue";
import { useScroll } from "@vueuse/core";
const scrollbox = ref(null);
const scroll = useScroll(scrollbox);
</script>

<style>
div.ex1 {
  background-color: black;
  width: 200px;
  height: 200px;
  overflow: scroll;
}
</style>
