<script setup>
import { ref, onMounted, onBeforeUnmount, nextTick } from 'vue'
import BgCircles from '@/components/BgCircles.vue';
import Navbar from '@/components/Navbar.vue'
import Cta from '@/components/Cta.vue'
import Footer from '@/components/Footer.vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const work = [
  {
    src: new URL('@/assets/images/icon/design.png', import.meta.url).href,
    title: "Desain",
    desc: "Merancang tampilan website menggunakan tools desain modern yaitu Figma"
  },
  {
    src: new URL('@/assets/images/icon/code.png', import.meta.url).href,
    title: "Development",
    desc: "Mempelajari struktur halaman web, layout, serta penggunaan bahasa dan tools"
  },
  {
    src: new URL('@/assets/images/icon/people.png', import.meta.url).href,
    title: "Kolaboratif",
    desc: "Bekerja sama dalam tim untuk membuat proyek website dari awal hingga selesai"
  },
  {
    src: new URL('@/assets/images/icon/presentation.png', import.meta.url).href,
    title: "Presentasi",
    desc: "Melatih kemampuan menyampaikan ide dan menampilkan hasil karya"
  }
]

const cardRefs = ref([])

function setCardRef(el, i) {
  if (el) cardRefs.value[i] = el
}

const activeIndex = ref(0)
let intervalId = null

onMounted(() => {
  // Animasi scroll GSAP untuk desktop/tablet
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

  // Carousel otomatis di mobile
  intervalId = setInterval(() => {
    activeIndex.value = (activeIndex.value + 1) % work.length
  }, 2500)
})

onBeforeUnmount(() => {
  if (intervalId) clearInterval(intervalId)
})
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">
      <BgCircles />
      <Navbar />

      <section class="z-50">
        <div class="max-w-[1100px] mx-auto max-xl:mx-5">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Ekstrakurikuler Jurusan</h1>
            <div class="mx-auto text-center">
              <p class="text-base font-medium text-white"><a href="/" class="mr-3">Beranda</a> <span class="mr-3 text-gray-300">/</span> Ekstrakurikuler</p>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1100px] mx-auto max-xl:mx-5">
            <div class="flex justify-between items-center flex-wrap">
                <div class="max-w-xl space-y-5">
                    <h1 class="sm:text-4xl text-3xl text-slate-800 font-semibold tracking-wide">Zone of Infomation Technology</h1>
                    <p class="text-lg font-medium text-slate-600">
                        Ekstrakurikuler yang berfokus pada <span class="font-semibold text-slate-800">pengembangan website</span> mulai dari <span class="font-semibold text-slate-800">desain UI/UX hingga Pemrograman</span>. Kegiatan ini membekali siswa dengan <span class="font-semibold text-slate-800">pengalaman dan keterampilan digital</span> untuk masa depan.
                    </p>
                    <div class="flex gap-3 flex-wrap pt-3">
                      <div class="space-y-3">
                        <div class="flex gap-x-3 items-center">
                          <img src="/src/assets/images/icon/check.png" class="w-7" alt="">
                          <p class="text-base font-semibold text-slate-800">Meningkatkan Skil</p>
                        </div>
                        <div class="flex gap-x-3 items-center">
                          <img src="/src/assets/images/icon/check.png" class="w-7" alt="">
                          <p class="text-base font-semibold text-slate-800">Membangun Portfolio</p>
                        </div>
                      </div>
                      <div class="space-y-3">
                        <div class="flex gap-x-3 items-center">
                          <img src="/src/assets/images/icon/check.png" class="w-7" alt="">
                          <p class="text-base font-semibold text-slate-800">Kreatif, Kolaboratif, Produktif</p>
                        </div>
                        <div class="flex gap-x-3 items-center">
                          <img src="/src/assets/images/icon/check.png" class="w-7" alt="">
                          <p class="text-base font-semibold text-slate-800">Asah Logika</p>
                        </div>
                      </div>
                    </div>
                </div>
                <div class="relative overflow-hidden z-0">
                    <img src="/src/assets/images/zit.png" class="object-cover w-[420px] z-50" alt="">
                </div>
            </div>
        </div>
      </section>

      <!-- Desktop Cards -->
      <section class="bg-primary py-20">
        <div class="max-w-[1100px] flex-wrap gap-10 justify-center mx-auto max-xl:mx-5 hidden sm:flex">
          <div
            v-for="(item, i) in work"
            :key="item.title"
            :ref="el => setCardRef(el, i)">
            <div class="relative w-[235px] h-[232px] rounded-3xl bg-slate-50 border-t-2 border-t-slate-300 border-b-2 border-b-slate-300 py-5 px-8">
              <img src="/src/assets/images/bg-line.png" class="absolute right-0 top-0 w-72" alt="">
              <div class="space-y-2">
                <img :src="item.src" class="w-16" alt="">
                <h1 class="text-xl text-slate-800 font-semibold">{{ item.title }}</h1>
                <p class="text-sm font-medium text-slate-600">{{ item.desc }}</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Mobile Cards -->
        <div class="sm:hidden flex justify-center">
          <div class="relative w-[90vw] max-w-xs h-[250px] flex items-center overflow-hidden">
            <transition name="slide-x" mode="out-in">
              <div
                v-if="work[activeIndex]"
                :key="work[activeIndex].title"
                class="absolute left-0 top-0 w-full h-full flex flex-col items-center justify-center transition-all duration-500"
                style="z-index: 2;"
              >
                <div class="relative w-full h-[252px] rounded-3xl bg-slate-50 border-t-2 border-t-slate-300 border-b-2 border-b-slate-300 py-8 px-8">
                  <img src="/src/assets/images/bg-line.png" class="absolute right-0 top-0 w-72" alt="">
                  <div class="space-y-2 flex flex-col">
                    <img :src="work[activeIndex].src" class="w-20" alt="">
                    <h1 class="text-xl text-slate-800 font-semibold">{{ work[activeIndex].title }}</h1>
                    <p class="text-sm font-medium text-slate-600">{{ work[activeIndex].desc }}</p>
                  </div>
                </div>
              </div>
            </transition>
          </div>
        </div>
      </section>

      <Cta />
      <Footer />
    </div>
  </main>
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