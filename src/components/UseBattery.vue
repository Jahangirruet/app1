<script setup>
import { useBattery } from "@vueuse/core";

const charging = useBattery();
const chargingTime = useBattery();
const dischargingTime = useBattery();
const level = useBattery();
console.log(charging);
</script>

<style></style>

<template>
  <template v-for="item in charging" :key="item.name">
    <li>{{ item }}</li>
  </template>
  <br />
  <template v-for="item1 in chargingTime" :key="item1.name">
    <li>{{ item1 }}</li>
  </template>
  <br />
  <template v-for="item2 in dischargingTime" :key="item2.name">
    <li>{{ item2 }}</li>
  </template>
  <br />
  <template v-for="item3 in level" :key="item3.name">
    <li>{{ item3 }}</li>
  </template>
  <br />
</template>
