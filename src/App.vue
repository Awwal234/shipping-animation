<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <RouterView />
</template>

<style>
* {
  box-sizing: border-box;
}

html {
  height: 100%;
}

body,
main {
  min-height: 100vh;
  font-family: 'Montserrat', sans-serif;
}

body::-webkit-scrollbar {
  width: 4px;
}

body::-webkit-scrollbar-track {
  width: 4px;
  background: #fff;
}

body::-webkit-scrollbar-thumb {
  width: 4px;
  background: #111;
}
</style>
