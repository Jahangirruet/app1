<template>
  <div>
    <div>
        {{ isDark }}
    </div>
    <div>
        <button @click="toggleDark">Toggle Dark mode</button>
    </div>
  </div>
</template>

<script>
import { useDark,useToggle } from '@vueuse/components';
const isDark = useToggle();
const toggleDark = useToggle(isDark);
</script>

<style>

</style>