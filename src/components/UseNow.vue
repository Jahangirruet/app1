<template>
  <div>
    {{ now }}
  </div>
</template>

<script setup lang="ts">
import { useNow,useDateFormat  } from "@vueuse/core";
const now = useDateFormat(useNow(), "YYYY-MM-DD-HH-MM-ss-SSSSSSSSSSSSSSSSSSSSSSSSSSSSSS");
</script>

<style></style>
