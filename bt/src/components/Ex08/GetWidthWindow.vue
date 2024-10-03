<template>
  <div>
    <h3>Bài 8:</h3>
    <p>Chiều rộng của cửa sổ: {{ windowWidth }} px</p>
    <br />*****************************************
  </div>
</template>
  
  <script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";

const windowWidth = ref(window.innerWidth); 
const updateWindowWidth = () => {
  windowWidth.value = window.innerWidth;
};

onMounted(() => {
  window.addEventListener("resize", updateWindowWidth);
});

onBeforeUnmount(() => {
  window.removeEventListener("resize", updateWindowWidth);
});
</script>
  
  <style  >
</style>
  