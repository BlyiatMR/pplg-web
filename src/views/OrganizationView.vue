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
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Ekstrakurikuler Jurusan</h1>
            <div class="mx-auto text-center">
              <p class="text-base font-medium text-white"><a href="/" class="mr-3">Beranda</a> <span class="mr-3 text-gray-300">/</span> Ekstrakurikuler</p>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
            <div class="flex justify-around items-center flex-wrap">
                <div class="max-w-xl space-y-5">
                    <h1 class="sm:text-4xl text-3xl text-slate-800 font-semibold tracking-wide">Zone of Infomation Technology</h1>
                    <p class="sm:text-lg text-base font-medium text-slate-600">
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

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
          <div class="flex justify-around gap-16 items-center flex-wrap">
            <div class="relative z-0 group">
              <div class="absolute left-8 -rotate-[4deg] w-[480px] h-[380px] bg-yellow-400 opacity-50 rounded-3xl -z-50 group-hover:-rotate-[8deg] duration-300"></div>
              <img src="/src/assets/images/model.jpg" class="object-cover w-[480px] h-[380px] rounded-3xl" alt="">
            </div>
            <div class="max-w-lg space-y-5">
              <h1 class="font-medium sm:text-4xl text-3xl text-slate-800 tracking-wide">Bagaimana jika siswa jurusan lain <span class="font-bold">ingin bergabung?</span></h1>
              <p class="sm:text-lg text-base font-medium text-slate-600">Zone IT sangat terbuka untuk semua siswa dari berbagai jurusan yang memiliki minat di bidang pengembangan website. Punya rasa ingin tahu, niat belajar, dan komitmen untuk berkembang bersama tim.</p>
              <div class="flex pt-5 gap-10">
                <a id="btn" href="#about" class="flex w-[220px] justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-semibold hover:w-[230px] duration-300">Gabung ZoneIT <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
              </div>
            </div>
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