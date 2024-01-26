<script lang="ts" setup>
import { ref } from 'vue';
import gsap from 'gsap'
const layout = ref(false);
const tp = ref(false);
const tc = ref(false);
const name = ref("");
const email = ref("");
const message = ref("");

const mailBox = ref(false);

const sendMail = () => {
    mailBox.value = true;
    setTimeout(() => {
        mailBox.value = false;
    }, 3000)
}

const toggleLayout = () => {
    layout.value = !layout.value
    gsap.fromTo('.layout', { x: 0, y: 0, opacity: 1, duration: 4 }, { x: 0, y: -0, opacity: 0, ease: 'step(6)' })
}
const openLayout = () => {
    layout.value = !layout.value
    tc.value = false;
    tp.value = true;
    gsap.fromTo('.layout', { x: 0, y: -0, opacity: 0, duration: 4 }, { x: 0, y: 0, opacity: 1, ease: 'step(6)' })
}
const openLayoutTwo = () => {
    layout.value = !layout.value
    tp.value = false;
    tc.value = true;
    gsap.fromTo('.layout', { x: 0, y: -0, opacity: 0, duration: 4 }, { x: 0, y: 0, opacity: 1, ease: 'step(6)' })
}
</script>

<template>
    <div>
        <div
            class="w-full mb-[40px] clash text-[11px] md:text-[18px] bg-[#000] px-[25px] py-[30px] md:py-[30px] md:px-[80px]">
            <div
                class="mb-[40px] mx-auto text-center md:mt-[80px] aeonikregular text-[25px] md:text-[30px] lg:text-[50px] lg:font-bold font-[600] leading-[120%] text-[#8491a0]">
                Features
            </div>
            <div
                class="hidden md:flex mb-[30px] space-x-[30px] px-[25px] md:px-[100px] items-center mx-auto w-full md:mx-[0px]">
                <div class="md:w-[18%]">
                    <img @click="openLayout" src="/image/techpoint.png" class="w-full" />
                </div>
                <div class="md:w-[18%]">
                    <a target="blank"
                        href="https://www.startupgrind.com/events/details/startup-grind-lagos-presents-we=are-hosting-gerald-okonkwo-ceo-parkit"><img
                            src="/image/startupgrind.png" class="w-full" /></a>
                </div>
                <div class="md:w-[18%]">
                    <img @click="openLayoutTwo" src="/image/techcabal.png" class="w-full" />
                </div>
                <div class="md:w-[18%]">
                    <a target="blank" href="https://www.benjamindada.com/mergers-acquisitions-african-startups-growth/"><img
                            src="/image/DB.png" class="w-full cursor-pointer" /></a>
                </div>
                <div class="md:w-[18%]">
                    <a target="blank" href="https://x.com/heritagebankplc/status/1051846794332827648?s=46"><img
                            src="/image/heritagebank.png" class="w-full" /></a>
                </div>
            </div>
            <!-- mobile -->
            <div
                class="flex md:hidden mb-[30px] space-x-[30px] px-[25px] md:px-[100px] items-center mx-auto w-full md:mx-[0px]">
                <div class="w-[30%]">
                    <img @click="openLayout" src="/image/techpoint.png" class="w-full" />
                </div>
                <div class="w-[30%]">
                    <a target="blank"
                        href="https://www.startupgrind.com/events/details/startup-grind-lagos-presents-we=are-hosting-gerald-okonkwo-ceo-parkit"><img
                            src="/image/startupgrind.png" class="w-full" /></a>
                </div>
                <div class="w-[30%]">
                    <img @click="openLayoutTwo" src="/image/techcabal.png" class="w-full" />
                </div>
            </div>
            <div
                class="flex md:hidden mb-[30px] space-x-[30px] px-[25px] md:px-[100px] items-center mx-auto w-full md:mx-[0px]">
                <div class="w-[30%]">
                    <a target="blank"
                        href="https://businessday.ng/news/article/fixit45-acquires-parkit-unveils-subscription-based-vip-programme/"><img
                            src="/image/businessday.png" class="w-full" /></a>
                </div>
                <div class="w-[30%]">
                    <a target="blank"
                        href="https://www.vanguardngr.com/2021/12/parkit-founder-gerald-okonkwo-appointed-ecowas-youth-ambassador/"><img
                            src="/image/Vanuar.png" class="w-full" /></a>
                </div>
                <div class="w-[30%]">
                    <a target="blank"
                        href="https://www.thisdaylive.com/index.php/2021/11/27/fixit45-acquires-parkit-unveils-subscription-based-vip-programme"><img
                            src="/image/thisday.png" class="w-full" /></a>
                </div>
            </div>
            <div
                class="flex md:hidden mb-[30px] space-x-[30px] px-[25px] md:px-[100px] items-center mx-auto w-[70%] md:mx-[0px]">
                <div class="w-[40%]">
                    <a target="blank" href="https://x.com/heritagebankplc/status/1051846794332827648?s=46"><img
                            src="/image/heritagebank.png" class="w-full mx-auto" /></a>
                </div>
                <div class="w-[30%]">
                    <a target="blank" href="https://www.benjamindada.com/mergers-acquisitions-african-startups-growth/"><img
                            src="/image/DB.png" class="w-full mx-auto" /></a>
                </div>
            </div>
            <div
                class="flex md:hidden mb-[30px] space-x-[30px] px-[25px] md:px-[100px] items-center mx-auto w-[70%] md:mx-[0px]">
                <div class="w-[35%]">
                    <a target="blank"
                        href="https://kenyanwallstreet.com/innovation-catalysts-operators-shaping-the-future-of-africas-tech-startups/"><img
                            src="/kenwall.png" class="w-[60px] h-[60px] mx-auto" /></a>
                </div>
                <div class="w-[35%]">
                    <a target="blank"
                        href="https://lawverse.com.ng/wp-content/uploads/2023/11/LAWVERSE-MAGAZINE-ISSUE-8.pdf"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYUA6Uxg2SywPldrMPA5Cnva83PlO53UuCrTMs3wdU27NsEccVPTSp2wfP&s=10"
                            class="w-full mx-auto" /></a>
                </div>
            </div>
            <!-- end mobile -->
            <div
                class="hidden md:flex mb-[25px] md:mb-[30px] md:space-x-[30px] space-y-[25px] md:space-y-[0px] px-[25px] md:px-[100px] md:items-center w-[80%] md:justify-center mx-auto md:w-[100%] md:mx-auto">
                <div class="md:w-[18%]">
                    <a target="blank"
                        href="https://businessday.ng/news/article/fixit45-acquires-parkit-unveils-subscription-based-vip-programme/"><img
                            src="/image/businessday.png" class="w-full" /></a>
                </div>
                <div class="md:w-[18%]">
                    <a target="blank"
                        href="https://www.vanguardngr.com/2021/12/parkit-founder-gerald-okonkwo-appointed-ecowas-youth-ambassador/"><img
                            src="/image/Vanuar.png" class="w-full" /></a>
                </div>
                <div class="md:w-[18%]">
                    <a target="blank"
                        href="https://www.thisdaylive.com/index.php/2021/11/27/fixit45-acquires-parkit-unveils-subscription-based-vip-programme"><img
                            src="/image/thisday.png" class="w-full" /></a>
                </div>
            </div>
            <div
                class="hidden md:flex mb-[25px] md:mb-[30px] md:space-x-[30px] space-y-[25px] md:space-y-[0px] px-[25px] md:px-[100px] md:items-center w-[80%] md:justify-center mx-auto md:w-[100%] md:mx-auto">
                <div class="md:w-[18%]">
                    <a target="blank"
                        href="https://kenyanwallstreet.com/innovation-catalysts-operators-shaping-the-future-of-africas-tech-startups/"><img
                            src="/kenwall.png" class="w-[100px] h-[100px] mx-auto" /></a>
                </div>
                <div class="md:w-[18%]">
                    <a target="blank"
                        href="https://lawverse.com.ng/wp-content/uploads/2023/11/LAWVERSE-MAGAZINE-ISSUE-8.pdf"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYUA6Uxg2SywPldrMPA5Cnva83PlO53UuCrTMs3wdU27NsEccVPTSp2wfP&s=10"
                            class="w-full" /></a>
                </div>
            </div>
        </div>
        <!-- send gerald black a message section -->
        <div
            class="w-full contactsection md:flex md:items-baseline md:space-x-[8px] bg-[#fff3e4] px-[25px] py-[60px] md:py-[120px] md:px-[80px]">
            <div class="md:w-[60%] mb-[40px] md:mb-[0px] w-full">
                <div class="text-[#000] mb-[15px] clash text-[32px] md:text-[55px] font-[700]">Let&apos;s talk business
                </div>
                <div class="text-[#8491a0] md:w-[70%] aeoniklight text-[15px] md:text-[18px] font-[400] leading-[150%]">
                    Now that you know a lot about me, let me know if you are interested to work with me.
                </div>
            </div>
            <!-- form -->
            <div class="md:w-[40%] w-full">
                <form method="POST" action="https://formspree.io/f/mzbndjbo">
                    <div class="text-[#000] mb-[8px] aeoniklight text-[16px] font-[400] leading-[150%]">Name</div>
                    <div class="w-full mb-[10px]">
                        <input v-model="name" name="name" autocomplete="false" type="text"
                            class="w-full px-[8px] py-[12px] aeoniklight text-[18px] rounded-[6px] border border-[#181823] focus:outline-none" />
                    </div>
                    <div class="text-[#000] mb-[8px] aeoniklight text-[16px] font-[400] leading-[150%]">Email</div>
                    <div class="w-full mb-[10px]">
                        <input v-model="email" name="email" id="email-address" autocomplete="false" type="email"
                            class="w-full px-[8px] py-[12px] aeoniklight text-[18px] rounded-[6px] border border-[#181823] focus:outline-none" />
                    </div>
                    <div class="text-[#000] mb-[8px] aeoniklight text-[16px] font-[400] leading-[150%]">Message</div>
                    <div class="w-full md:mb-[10px]">
                        <textarea v-model="message" name="message" autocomplete="false" type="text"
                            class="w-full px-[8px] message pt-[6px] pb-[90px] aeoniklight text-[18px] rounded-[6px] border border-[#181823] focus:outline-none"></textarea>
                    </div>
                    <div v-show="mailBox" class="mt-[10px] mb-[10px]">
                        Sent successfully
                    </div>
                    <button type="submit" @click="sendMail"
                        class="w-full mt-[20px] cursor-pointer text-[#fff] text-center bg-[#000] px-[8px] py-[12px] aeoniklight text-[18px] rounded-[6px] border border-[#181823]">
                        Send a message
                    </button>
                </form>
            </div>
            <!-- end form -->
        </div>
        <!--end message section-->
        <div class="px-[25px] md:flex md:justify-between md:items-center py-[45px] md:px-[80px] w-full bg-[#000]">
            <div class="flex mb-[10px] md:mb-[0px] item-center space-x-[9px]">
                <div class="">
                    <img src="/image/GBlogo.svg" class="cursor-pointer w-[30px] h-[30px] md:w-[42px] md:h-[42px]"
                        loading="lazy" />
                </div>
                <div class="clash relative top-[1px] md:top-[4px] text-[20px] font-[700] text-[#fff]">Gerald Black</div>
            </div>
            <div class="aeoniklight text-[#fff] text-[15px] font-[400]">All Right Reserved. Gerald Black</div>
        </div>
        <!--footer-->
        <!--overlay for features-->
        <div v-show="layout"
            class="w-full layout py-[20px] px-[25px] md:px-[80px] bg-[#000] fixed top-0 z-[2000] left-0 h-full">
            <div class="w-full mb-[80px] flex items-center justify-between">
                <div></div>
                <div>
                    <svg @click="toggleLayout" xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 14 14"
                        fill="none">
                        <path d="M11.0827 2.91666L2.91602 11.0833M2.91602 2.91666L11.0827 11.0833" stroke="white"
                            stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                </div>
            </div>
            <div v-show="tp"
                class="space-y-[20px] text-left cursor-pointer text-[13px] md:text-[23px] font-[600] text-[#fff]">
                <div class="underline w-fit"><a target="blank" referrer="no-referrer"
                        href="https://techpoint.africa/2023/08/24/tech-operators-mixer-2023-spotlighting-the-unsung-heroes-of-the-african-tech-space">https://techpoint.africa/2023/08/24/tech-operators-mixer-2023-spotlighting-the-unsung-heroes-of-the-african-tech-space</a>
                </div>
                <div class="underline w-fit"><a target="blank" referrer="no-referrer"
                        href="https://techpoint.africa/2023/03/14/gerald-black-okonkwo-parkit-founder">https://techpoint.africa/2023/03/14/gerald-black-okonkwo-parkit-founder</a>
                </div>
            </div>
            <div v-show="tc"
                class="space-y-[20px] text-left cursor-pointer text-[13px] md:text-[23px] font-[600] text-[#fff]">
                <div class="underline w-fit"><a target="blank"
                        href="https://techcabal.com/2023/11/04/black-ops-operators/">https://techcabal.com/2023/11/04/black-ops-operators/</a>
                </div>
                <div class="underline w-fit"><a target="blank" referrer="no-referrer"
                        href="https://techcabal.com/2022/03/22/building-parkit-gerald-okonkwo-schneider-komolafe/">https://techcabal.com/2022/03/22/building-parkit-gerald-okonkwo-schneider-komolafe/</a>
                </div>
            </div>
        </div>
        <!--end overlay for features-->
    </div>
</template>

<style scoped>
.message {
    word-wrap: break-word;
    overflow-wrap: break-word;
}
</style>