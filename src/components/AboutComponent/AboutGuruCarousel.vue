<template>
  <section class="bg-slate-50 py-20">
    <div class="max-w-[1240px] mx-auto max-xl:mx-5">
      <div class="flex flex-wrap gap-5 justify-around">
        <div class="max-w-lg sm:pt-10 pt-0 space-y-5">
          <h1 class="font-semibold sm:text-4xl text-3xl text-slate-800 tracking-wide leading-tight">
            Pengelola dan Tenaga Pendidik PPLG
          </h1>
          <p class="sm:text-lg text-base font-medium text-slate-600">
            Menampilkan jajaran pimpinan sekolah dan tenaga pendidik yang berperan dalam pelaksanaan pembelajaran di jurusan PPLG.
          </p>
        </div>
        <div class="flex flex-wrap justify-around gap-10 pb-20">
          <div
            v-for="(profile, idx) in profilesh"
            :key="idx"
            class="carousel-card relative max-w-[280px] bg-white rounded-3xl shadow-xl">
            <img :src="profile.img" class="rounded-t-3xl w-80 h-80 object-cover object-top" alt="" />
            <div class="justify-between items-end py-3 px-5">
              <div class="space-y-2">
                <p class="text-lg text-slate-800 font-semibold">
                  {{ profile.name }}
                </p>
              </div>
              <div class="flex items-center justify-between">
                <div>
                  <p class="w-40 text-base text-slate-600">
                    {{ profile.position }}
                  </p>
                </div>
                <div class="flex gap-3">
                  <a href="">
                    <i class="fa-brands fa-instagram text-slate-600 text-2xl"></i>
                  </a>
                  <a href="">
                    <i class="fa-brands fa-facebook text-slate-600 text-2xl"></i>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="relative overflow-hidden w-full pb-10">
        <!-- Shadow kanan kiri -->
        <div class="sm:flex hidden pointer-events-none absolute -top-20 -left-10 h-[50rem] w-20 z-20 bg-slate-50 blur-[14px]"></div>
        <div class="sm:flex hidden pointer-events-none absolute -top-20 -right-10 h-[50rem] w-20 z-20 bg-slate-50 blur-[14px]"></div>
        <!-- Carousel -->
        <div
          ref="carouselRef"
          class="flex gap-10"
          style="will-change: transform;">
          <div
            v-for="(profile, idx) in [...profiles, ...profiles, ...profiles]"
            :key="idx"
            class="carousel-card relative max-w-[280px] bg-white rounded-3xl shadow-xl">
            <img :src="profile.img" class="rounded-t-3xl w-80 h-80 object-cover object-top" alt="" />
            <div class="justify-between items-end py-3 px-5">
              <div class="space-y-2">
                <p class="text-lg text-slate-800 font-semibold">
                  {{ profile.name }}
                </p>
              </div>
              <div class="flex items-center justify-between">
                <div>
                  <p class="w-40 text-base text-slate-600">
                    {{ profile.position }}
                  </p>
                </div>
                <div class="flex gap-3">
                  <a href="">
                    <i class="fa-brands fa-instagram text-slate-600 text-2xl"></i>
                  </a>
                  <a href="">
                    <i class="fa-brands fa-facebook text-slate-600 text-2xl"></i>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- End Carousel -->
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(['profiles', 'profilesh'])
import { ref, onMounted, onUnmounted, nextTick, watch } from 'vue'
import gsap from 'gsap'

const carouselRef = ref(null)
let tl = null

async function startCarousel() {
  await nextTick()
  const cards = carouselRef.value?.querySelectorAll('.carousel-card')
  if (!cards || cards.length === 0) return
  const cardWidth = cards[0].offsetWidth + 40
  const originalCards = props.profiles.length
  const loopWidth = cardWidth * originalCards

  if (tl) tl.kill()
  tl = gsap.timeline({ repeat: -1, defaults: { ease: "none" } })
  tl.to(carouselRef.value, {
    x: `-=${loopWidth}`,
    duration: originalCards * 5,
    modifiers: {
      x: gsap.utils.unitize(x => parseFloat(x) % loopWidth)
    }
  })
}

onMounted(startCarousel)

watch(() => props.profiles, startCarousel, { deep: true })

onUnmounted(() => {
  if (tl) tl.kill()
})
</script>