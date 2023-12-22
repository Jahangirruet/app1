<template>
  <div>
    <input type="text" v-model="title" />
  </div>
</template>

<script setup>
import { useTitle } from '@vueuse/core';
const title = useTitle();
title.value = "my";
</script>

