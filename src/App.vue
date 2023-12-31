<script setup>
import History from "./components/RefHistory.vue";
import { useDark, useToggle, useColorMode } from "@vueuse/core";
const isDark = useDark();
const colorMode = useColorMode({
   attribute: "theme",
  modes: {
    dim: "dim",
    cafe: "cafe",
  },
});
const toggleDark = useToggle(isDark);
</script>

<template>
  <div>
    <div>
      {{ colorMode }}
    </div>
    <div>
      <button @click="toggleDark()">dark</button>
      <button @click="colorMode = 'light'">light</button>
      <button @click="colorMode = 'dim'">Dim</button>
      <button @click="colorMode = 'cafe'">Cafe</button>
    </div>
    <br />
    <p>
        <input type="text">
    </p>
    <br />
    <div>
    </div>
    <History />
  </div>
</template>

<style>
[theme="dark"]
 {
  background: black;
  color: white;
}
[theme="dim"]{
  background: gray;
  color: white;
}
[theme="cafe"]{
  background: #c0acac;
  color: white;
}
</style>
