<script setup lang="ts">
import Header from '../components/HeaderSect.vue';
import About from '../components/AboutSect.vue';
</script>

<template>
  <main class="bg-[#000] min-h-[100vh] w-full">
    <div class="first_section h-fit pt-[18px] px-[25px] md:pt-[20] md:px-[80px] w-full">
      <div class="fixed z-[1000] w-full left-0">
        <Header />
      </div>
      <div class="pt-[180px] md:pt-[190px] w-full md:w-[55%]">
        <div class="aeonikregular mb-[20px] md:mb-[35px] font-[500] text-[18px] md:text-[22px] text-[#fff]">Hey, I'm</div>
        <div class="clash text-[45px] mb-[20px] md:mb-[35px] text-wrap md:text-[80px] font-[700] text-[#fff]">
          Gerald Black
        </div>
        <div class="aeonikregular mb-[30px] md:mb-[46px] font-[500] text-[18px] md:text-[22px] text-[#fff]">
          I am the strategic architect, weaving ambition and expertise to sculpt triumphant narratives. Armed with a mind
          that navigates commerce intricacies, I orchestrate growth, turning potential into profit with every calculated
          move.
        </div>
        <div
          class="w-fit cursor-pointer space-x-[6px] rounded-[4px] py-[10px] px-[22px] flex items-center h-fit bg-[#3F3F46]">
          <div><img src="/image/mail.svg" class="mail z-[0]" /></div>
          <div class="aeonikregular font-[500] text-[16px] md:text-[18px] text-[#fff]">Work with me</div>
        </div>
        <div class="pb-[30px] md:pb-[90px]"></div>
      </div>
      <!-- endly -->
    </div>
    <div class="md:hidden mb-[30px] w-full h-fit">
      <img src="/image/geraldbgsmall.png" class="w-full h-[600px]" />
    </div>
    <About />
  </main>
</template>

<style scoped>
main {
  background: #111;
}

.first_section {
  background: url('/geraldbgbig.png');
  background-repeat: no-repeat;
  object-fit: contain;
  background-size: 100% 100%;
}

.mail {
  animation: 1s float linear infinite;
}

@keyframes float {
  0% {
    top: 0px;
    position: relative;
  }

  100% {
    top: -4px;
    position: relative;
  }
}

@media only screen and (max-width: 767px) {
  .first_section {
    background: #111;
    background-repeat: no-repeat;
    object-fit: contain;
    background-size: 100% 100%;
  }
}
</style>
