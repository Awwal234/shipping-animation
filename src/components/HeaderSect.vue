<script setup lang="ts">
import { ref } from 'vue'
const menuExtra = ref(false)

const toggleMenu = () => {
    menuExtra.value = !menuExtra.value
}
</script>

<template>
    <div
        class="bg-[#27272A] relative z-[1000] header mx-auto left-0 rounded-[10px] w-[95%] md:w-[90%] py-[18px] px-[20px] md:px-[117px]">
        <div class="w-full flex items-center justify-between">
            <div class="flex item-center space-x-[9px]">
                <div class="">
                    <img src="/image/GBlogo.svg" class="cursor-pointer w-[30px] h-[30px] md:w-[42px] md:h-[42px]"
                        loading="lazy" />
                </div>
                <div class="clash relative top-[1px] md:top-[4px] text-[20px] font-[700] text-[#fff]">GeraldBlack</div>
            </div>
            <div>
                <img @click="toggleMenu" src="/image/menu.svg"
                    class="cursor-pointer w-[30px] h-[30px] md:w-[42px] md:h-[42px]" loading="lazy" />
            </div>
        </div>
        <!-- extra section -->
        <div v-show="menuExtra">
            <div class="mt-[10px] mb-[40px] h-[3px] bg-[#2f2f2f]"></div>
            <div class="w-full">
                <div class="space-y-[20px] w-full mb-[20px] md:space-y-[0px] md:flex md:items-center">
                    <div
                        class="aeonikregular text-left md:w-[33.3%] cursor-pointer text-[40px] md:text-[40px] font-[700] text-[#fff]">
                        Podcast
                    </div>
                    <div
                        class="aeonikregular text-left md:w-[33.3%] cursor-pointer text-[40px] md:text-[40px] font-[700] text-[#fff]">
                        YouTube
                    </div>
                    <div
                        class="aeonikregular text-left md:w-[33.3%] cursor-pointer text-[40px] md:text-[40px] font-[700] text-[#fff]">
                        Contact
                    </div>
                </div>
                <div class="space-y-[20px] w-full mb-[20px] md:space-y-[0px] md:flex md:items-center">
                    <div
                        class="aeonikregular text-left w-[33.3%] cursor-pointer text-[40px] text-wrap md:text-[40px] font-[700] text-[#fff]">
                        Blog
                    </div>
                    <div
                        class="aeonikregular text-left w-[33.3%] cursor-pointer text-[40px] text-wrap md:text-[40px] font-[700] text-[#fff]">
                        Microblack
                    </div>
                    <div
                        class="aeonikregular w-[33.3%] text-left cursor-pointer text-[40px] text-wrap md:text-[40px] font-[700] text-[#fff]">
                        XConnect
                    </div>
                </div>
            </div>
        </div>
        <!-- end extra section -->
    </div>
</template>

<style scoped>
.header {
    box-shadow: 3px -3px 6px 0px rgba(0, 0, 0, 0.25);
}
</style>