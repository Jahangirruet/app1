<template>
  <div>
    <div>
      {{ counter }}
    </div>
    <p>
        <button @click="isActive ? pause():resume()">{{ isActive ? 'Pause':'Resume' }}</button>
        <br />
        <button @click="counter=0">Reset</button>
    </p>
  </div>
</template>

<script setup>
import { useInterval } from "@vueuse/core";
const {counter,pause,resume,isActive} = useInterval(1000,{controls: true});
</script>

<style></style>
