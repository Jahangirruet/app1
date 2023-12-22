<template>
  <div>
    {{ coords }}
  </div>
</template>

<script setup>
import { useGeolocation } from '@vueuse/core'

const coords = useGeolocation()
</script>

<style>

</style>