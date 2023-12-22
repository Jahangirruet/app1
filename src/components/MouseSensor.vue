<template>
  <div>
    <div
      class="ball"
      :style="{ top: position.x + 'px', left: position.y + 'px' }"
    >
      <div>OOOOOOOOO</div>
    </div>
  </div>
</template>

<script setup>
import { onKeyStroke } from "@vueuse/core";
import { ref } from "vue";

const controls = {
  ArrowDown: () => (position.value.y += 5),
  ArrayUp: () => (position.value.y -= 5),
  ArrayRight: () => (position.value.x += 5),
  ArrowLeft: () => (position.value.x -= 5),
};

onKeyStroke(Object.keys(controls), (e) => {
  e.preventDefault();
  controls[e.key]();
});

const position = ref({ x: 0, y: 0 });

</script>

<style>
.ball {
  widows: 10px;
  height: 10px;
  background: red;
  border-radius: 100%;
  position: absolute;
}
</style>
