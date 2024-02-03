<script setup lang="ts">
import { ref, onMounted } from 'vue'
import gsap from 'gsap';
const shipText = ref(true)
const open = ref(false)
const packageIcon = ref(true)
const line = ref(false)
const light = ref(false)
const optimusoff = ref(true)
const shipOrdered = ref(false)
const first = ref(false)

const packageAnime = () => {
  shipText.value = false;
  first.value = true;
  setTimeout(() => {
    open.value = true;
  }, 2000);
  setTimeout(() => {
    gsap.fromTo('#package', { x: 0, y: 0 }, { x: 45, y: 0, ease: 'power1.out' });
  }, 3000);
  setTimeout(() => {
    open.value = false;
    packageIcon.value = false;
  }, 5000);
  setTimeout(() => {
    gsap.fromTo('#optimus', { x: 0, y: 0 }, { x: -50, y: 0, ease: 'power1.in' });
    line.value = true;
  }, 5000);
  setTimeout(() => {
    gsap.fromTo('#optimuslight', { x: -50, y: 0 }, { x: 140, y: 0, duration: 4, ease: 'power1.in' });
    optimusoff.value = false;
    light.value = true;
    setTimeout(() => {
      line.value = false;
      first.value = false;
      light.value = false;
      shipOrdered.value = true;
    }, 5000)
  }, 6000);
}
</script>

<template>
  <main class="bg-[#ffdf80] hidden lg:flex items-center justify-center min-h-[100vh] w-full">
    <div @click="packageAnime"
      class="w-[230px] overflow-hidden bg-[#000] cursor-pointer text-center h-fit rounded-[600px]">
      <div v-show="shipText" class="plus text-[#fff] py-[18px] text-[16px]">Ship Order</div>
      <div v-show="first" class="flex space-x-[30px] justify-center py-[11px] items-center">
        <div v-show="packageIcon" id="package" class="w-fit z-[150] h-fit"><img src="/package.svg"
            class="w-[10px] h-[10px]" />
        </div>
        <div v-show="optimusoff" id="optimus" class="w-fit z-[200] h-fit relative"><img
            :src="open ? 'optimusopen.svg' : '/optimusclosed.svg'" class="w-[60px] h-[40px]" /></div>
        <div v-show="light" id="optimuslight" class="w-fit z-[200] h-fit relative"><img src="/optimuslight.svg"
            class="w-[80px] h-[41px]" /></div>
      </div>
      <div v-show="shipOrdered" class="flex space-x-[4px] py-[18px] justify-center items-center">
        <div class="plus text-[#fff] text-[16px]">Order Shipped</div>
        <div id="tick" class="w-fit z-[200] h-fit relative"><img src="/tick.svg" class="w-[13px] h-[13px]" /></div>
      </div>
      <div v-show="line" class="absolute z-[100] mt-[-32px] w-fit h-fit"><img src="/roadline.svg"
          class="w-[230px] h-[2px]" /></div>
    </div>
  </main>
</template>

<style scoped>
main {
  background: #ffdf80;
}
</style>
