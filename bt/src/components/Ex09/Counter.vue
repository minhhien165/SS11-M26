<template>
    <div>
      <h3>Bài 9:</h3>
      <h4>Ứng dụng đếm số</h4>
      <p>Count: {{ count }}</p>
      <br>***************************************
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onBeforeUnmount } from 'vue';
  
  const count = ref(0);  
  let intervalId;  
  const incrementCount = () => {
    count.value++;
  };
  
  onMounted(() => {
    intervalId = setInterval(incrementCount, 1000);
  });
  
  onBeforeUnmount(() => {
    clearInterval(intervalId); 
  });
  </script>
  
  <style  >
  </style>
  