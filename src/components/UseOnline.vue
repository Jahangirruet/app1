<template>
  <div>
    {{ online }}
  </div>
</template>

<script setup>
import { useOnline } from '@vueuse/core';
const online = useOnline()
console.log(online)

</script>

<style>

</style>