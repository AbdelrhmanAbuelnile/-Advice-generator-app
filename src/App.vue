<script setup>
import Card from './components/Card.vue'
</script>

<template>
<div class="page max-sm:px-2">
  <Card/>
  <p class="text-Light-Cyan text-xs text-center md:text-xl">
    Challenge by
     <a href="https://www.frontendmentor.io" class="text-Neon-Green" target="_blank">Frontend Mentor</a>. Coded by 
     <a href="https://github.com/AbdelrhmanAbuelnile" class="text-Neon-Green" target="_blank">Abdelrhman</a> 💚
  </p>
</div>
</template>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@200;300;400;500;600;700;800&display=swap');

* {
  font-family: 'Manrope', sans-serif;
}
.page{
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background:  hsl(218, 23%, 16%);
}
p {
  position: absolute;
  bottom: 0;
  transform: translateY(-50%);
}
</style>
