<script setup>
import { ref, onMounted, onBeforeUnmount, nextTick } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

const props = defineProps(['work'])
const cardRefs = ref([])
function setCardRef(el, i) {
  if (el) cardRefs.value[i] = el
}
const activeIndex = ref(0)
let intervalId = null

onMounted(() => {
  gsap.registerPlugin(ScrollTrigger)
  nextTick(() => {
    cardRefs.value.forEach((el, i) => {
      if (el) {
        gsap.fromTo(
          el,
          { y: 40, opacity: 0 },
          {
            y: 0,
            opacity: 1,
            duration: 0.7,
            delay: i * 0.2,
            ease: "power2.out",
            scrollTrigger: {
              trigger: el,
              start: "top 90%",
              toggleActions: "play none none none"
            }
          }
        )
      }
    })
  })
  intervalId = setInterval(() => {
    activeIndex.value = (activeIndex.value + 1) % props.work.length
  }, 2500)
})

onBeforeUnmount(() => {
  if (intervalId) clearInterval(intervalId)
})
</script>

<template>
  <section class="bg-primary py-20">
    <div class="max-w-[1240px] flex-wrap gap-10 justify-center mx-auto max-xl:mx-5 hidden sm:flex">
      <div
        v-for="(item, i) in work"
        :key="item.title"
        :ref="el => setCardRef(el, i)">
        <div class="relative w-[255px] h-full rounded-3xl bg-slate-50 border-t-2 border-t-slate-300 border-b-2 border-b-slate-300 py-5 px-8">
          <img src="/src/assets/images/bg-line.png" class="absolute right-0 top-0 w-72" alt="">
          <div class="space-y-2">
            <img :src="item.src" class="w-16" alt="">
            <h1 class="text-xl text-slate-800 font-semibold">{{ item.title }}</h1>
            <p class="text-md font-medium text-slate-600">{{ item.desc }}</p>
          </div>
        </div>
      </div>
    </div>
    <!-- Mobile Cards -->
    <div class="sm:hidden flex justify-center">
      <div class="relative w-[90vw] max-w-xs h-[280px] flex items-center overflow-hidden">
        <transition name="slide-x" mode="out-in">
          <div
            v-if="work[activeIndex]"
            :key="work[activeIndex].title"
            class="absolute left-0 top-0 w-full h-full flex flex-col items-center justify-center transition-all duration-500"
            style="z-index: 2;">
            <div class="relative w-full h-[280px] rounded-3xl bg-slate-50 border-t-2 border-t-slate-300 border-b-2 border-b-slate-300 py-8 px-8">
              <img src="/src/assets/images/bg-line.png" class="absolute right-0 top-0 w-72" alt="">
              <div class="space-y-2 flex flex-col">
                <img :src="work[activeIndex].src" class="w-20" alt="">
                <h1 class="text-xl text-slate-800 font-semibold">{{ work[activeIndex].title }}</h1>
                <p class="text-md font-medium text-slate-600">{{ work[activeIndex].desc }}</p>
              </div>
            </div>
          </div>
        </transition>
      </div>
    </div>
  </section>
</template>

<style scoped>
.slide-x-enter-active, .slide-x-leave-active {
  transition: all 0.5s cubic-bezier(.55,0,.1,1);
  position: absolute;
  width: 100%;
}
.slide-x-enter-from {
  opacity: 0;
  transform: translateX(60px);
}
.slide-x-leave-to {
  opacity: 0;
  transform: translateX(-60px);
}
.slide-x-enter-to, .slide-x-leave-from {
  opacity: 1;
  transform: translateX(0);
}
</style>