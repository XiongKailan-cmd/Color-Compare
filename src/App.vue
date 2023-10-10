
  
<template>
  <div id="main" @click.stop="otherAreaClick">
    <Color ref="color" />
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Color from "./views/Color/index.vue";

const color = ref(null);

const otherAreaClick = () => {
  (color.value as any).changeColor("#FFFFF3");
}

</script>

<style scoped>
#main {
  width: 100%;
  height: 100%;
}
</style>
