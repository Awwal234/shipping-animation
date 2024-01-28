<script setup lang="ts">
import { ref } from 'vue'
import gsap from 'gsap'
import { ScrollToPlugin } from 'gsap/all'

gsap.registerPlugin(ScrollToPlugin)
const menuExtra = ref(false)

const toggleMenu = () => {
    menuExtra.value = !menuExtra.value
    gsap.fromTo('.slide', { y: -10, opacity: 0 }, { y: 0, opacity: 1, ease: 'power1. in' })
}

const goTo = (url: string) => {
    //@ts-ignore
    window.location.assign(url);
    menuExtra.value = !menuExtra.value
}

const toContact = () => {
    gsap.to(window, { duration: 2, scrollTo: '.contactsection' })
    menuExtra.value = !menuExtra.value
}
const toTop = () => {
    gsap.to(window, { duration: 2, scrollTo: '.porttop' })
}
</script>

<template>
    <div
        class="bg-[#27272A] relative z-[1000] header mx-auto left-0 rounded-[10px] w-[95%] md:w-[90%] py-[18px] px-[20px] md:px-[117px]">
        <div class="w-full flex items-center justify-between">
            <div @click="toTop" class="flex md:cursor-pointer item-center space-x-[9px]">
                <div class="">
                    <img src="/image/GBlogo.svg" class="cursor-pointer w-[30px] h-[30px] md:w-[42px] md:h-[42px]"
                        loading="lazy" />
                </div>
                <div class="clash relative top-[1px] md:top-[4px] text-[20px] font-[700] text-[#fff]">Gerald Black</div>
            </div>
            <div>
                <img @click="toggleMenu" src="/image/menu.svg"
                    class="cursor-pointer w-[30px] h-[30px] md:w-[42px] md:h-[42px]" loading="lazy" />
            </div>
        </div>
        <!-- extra section -->
        <div v-show="menuExtra">
            <div class="mt-[10px] mb-[40px] h-[3px] bg-[#2f2f2f]"></div>
            <div class="w-full slide">
                <div class="space-y-[20px] w-full mb-[20px] md:space-y-[0px] md:flex md:items-center">
                    <div @click="goTo('https://podcasters.spotify.com/pod/show/backendbygeraldblack?')"
                        class="aeonikregular text-left md:w-[33.3%] cursor-pointer text-[17px] md:text-[20px] font-[700] text-[#fff]">
                        Podcast
                    </div>
                    <div @click="goTo('https://youtube.com/@geraldblack?si=oPfe44bXwyuflNUJ')"
                        class="aeonikregular text-left md:w-[33.3%] cursor-pointer text-[17px] md:text-[20px] font-[700] text-[#fff]">
                        YouTube
                    </div>
                    <div @click="goTo('https://xconnect.geraldblack.co/')"
                        class="aeonikregular text-left md:w-[33.3%] cursor-pointer text-[17px] md:text-[20px] font-[700] text-[#fff]">
                        Blog
                    </div>
                </div>
                <div class="space-y-[20px] w-full mb-[20px] md:space-y-[0px] md:flex md:items-center">
                    <div @click="goTo('https://www.techbygerald.com/?m=1')"
                        class="aeonikregular text-left w-[33.3%] cursor-pointer text-[17px] text-wrap md:text-[20px] font-[700] text-[#fff]">
                        XConnect
                    </div>
                    <div @click="goTo('https://microblack.geraldblack.co/')"
                        class="aeonikregular text-left w-[33.3%] cursor-pointer text-[17px] text-wrap md:text-[20px] font-[700] text-[#fff]">
                        Microblack
                    </div>
                    <div @click="toContact()"
                        class="aeonikregular w-[33.3%] text-left cursor-pointer text-[17px] text-wrap md:text-[20px] font-[700] text-[#fff]">
                        Contact
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