<script setup>
import { onMounted, ref } from 'vue'
import gsap from 'gsap'

const root = ref(null)

onMounted(() => {
  const leftCircles = gsap.utils.toArray('.bg-circle-left', root.value)
  const rightCircles = gsap.utils.toArray('.bg-circle-right', root.value)

  gsap.from(leftCircles, {
    x: -200,
    opacity: 0,
    duration: 1.2,
    ease: "power2.out",
    stagger: 0.15,
  })
  gsap.from(rightCircles, {
    x: 200,
    opacity: 0,
    duration: 1.2,
    ease: "power2.out",
    stagger: 0.15,
  })
})
</script>

<template>
  <div
    class="max-w-[1100px] relative mx-auto pointer-events-none select-none"
    ref="root">
    <div class="w-[65rem] h-[65rem] bg-white rounded-full absolute -left-[45rem] opacity-10 -z-50 bg-circle-left"></div>
    <div class="w-[75rem] h-[75rem] bg-white rounded-full absolute -top-[5rem] -left-[45rem] opacity-10 -z-50 bg-circle-left"></div>
    <div class="sm:flex hidden w-[55rem] h-[55rem] border border-white rounded-full absolute top-20 -right-[45rem] opacity-10 -z-50 bg-circle-right"></div>
    <div class="sm:flex hidden w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[45rem] opacity-10 -z-50 bg-circle-right"></div>
    <div class="sm:flex hidden w-[75rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[45rem] opacity-10 -z-50 bg-circle-right"></div>
  </div>
</template>