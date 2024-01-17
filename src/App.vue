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

@font-face {
  font-family: clash;
  src: url(./fonts/ClashGrotesk-Variable.ttf);
}

@font-face {
  font-family: aeoniklight;
  src: url(./fonts/AeonikTRIAL-Light.otf);
}

@font-face {
  font-family: aeonikregular;
  src: url(./fonts/AeonikTRIAL-Regular.otf);
}

.clash {
  font-family: clash;
}

.aeoniklight {
  font-family: aeoniklight;
}

.aeonikregular {
  font-family: aeonikregular;
}

html {
  height: 100%;
}

body,
main {
  min-height: 100vh;
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
