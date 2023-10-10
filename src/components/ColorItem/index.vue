<template>
  <div id="item">
    <div class="color-show" :style="{ 'background-color': props.color }"></div>
    <div class="color-font">{{ props.color }}</div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  color: {
    type: String,
    default: "#FFFFFF",
  },
});


</script>

<style scoped>
#item {
  display: flex;
  place-items: center;
  /* place-content: center; */
  padding: 2px;
  box-sizing: border-box;
}

#item:hover {
  border: 1px solid #FF7F24;
  border-radius: 5px;
  color: #000;
  cursor: pointer;
}

.color-font:hover {
  color: #000;
}

.color-show {
  width: 30px;
  height: 30px;
  border-radius: 5px;
  margin-right: 10px;
  position: relative;
}
</style>