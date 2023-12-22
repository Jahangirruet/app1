<script setup>
import { ref } from "vue";
import { useClipboard } from "@vueuse/core";

const texToCopy = ref("hello world");
const { copy, text, copied, isSupported } = useClipboard({ source: texToCopy });
</script>

<template>
  <div>
    <input type="text" v-model="texToCopy" />
    <button @click="copy()">
      <!-- by default, `copied` will be reset in 1.5s -->
      <span v-if="!copied">Copy</span>
      <span v-else>Copied!</span>
    </button>
  </div>
</template>
