<template>
  <div>
    <input v-model="name">
    <br />
    {{ history }}
  </div>
</template>

<script setup>
import {ref} from "vue"
import { useRefHistory } from "@vueuse/core";
const name = ref("");
const { history } = useRefHistory(name);
</script>

<style>

</style>