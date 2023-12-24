<script setup lang="ts">
import { ref } from 'vue'
import { useInfiniteScroll } from '@vueuse/core'
import { load } from 'js-yaml';

const el = ref<HTMLElement | null>(null)
const data = ref([])
const total = ref(0)

loadData()

async function loadData() {
  if(true)
  return;
}
</script>

<template>
<div>
  <div ref="el" class="flex flex-col gap-2 p-4 w-300px h-300px m-auto overflow-y-scroll bg-gray-500/5 rounded">
    <div v-for="item in data" :key="item" class="h-15 bg-gray-500/5 rounded p-3">
      {{ item }}
    </div>
  </div>
</div>

</template>