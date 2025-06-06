<script setup>
import { ref, onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import img_curicullum from "@/assets/images/icon/icon-curicullum.png"
import img_computer from "@/assets/images/icon/icon-computer.png"
import img_job from "@/assets/images/icon/icon-job.png"
import img_people from "@/assets/images/icon/icon-people.png"

gsap.registerPlugin(ScrollTrigger)

const cardRefs = ref([])

const cards = [
  {
    title: "Kurikulum Up-to-date",
    description: "Kurikulum dirancang agar sejalan dengan perkembangan teknologi terkini, menjadikan siswa siap bersaing di pasar kerja.",
    src: img_curicullum,
  },
  {
    title: "Fasilitas Komputer",
    description: "Menyediakan lab komputer yang mendukung pengalaman belajar sesuai dengan kebutuhan industri saat ini.",
    src: img_computer,
  },
  {
    title: "Peluang Karir Luas",
    description: "Membuka jalan untuk berbagai profesi seperti web developer, mobile developer, UI/UX designer, atau pengembang IoT.",
    src: img_job,
  },
  {
    title: "Kegiatan Ekstrakurikuler",
    description: "Memiliki Ekstrakurikuler Zone IT, yang berfokus pada pembuatan website, mulai dari desain hingga pemrograman.",
    src: img_people,
  },
]

onMounted(() => {
  cardRefs.value.forEach((el, i) => {
    if (!el) return
    gsap.from(el, {
      opacity: 0,
      y: 60,
      duration: 0.7,
      delay: i * 0.15,
      ease: "power2.out",
      scrollTrigger: {
        trigger: el,
        start: "top 85%",
        toggleActions: "play none none none"
      }
    })
  })
})
</script>

<template>
  <section>
    <div class="max-w-[1100px] relative mx-auto max-xl:mx-5 py-20">
      <div class="w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[85rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[105rem] h-[85rem] border border-white rounded-full absolute -top-[10rem] -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[125rem] h-[85rem] border border-white rounded-full absolute -top-[10rem] -right-[30rem] opacity-10 -z-50"></div>

      <h1 class="sm:max-w-7xl mx-auto text-center font-semibold sm:text-4xl text-3xl text-white leading-tight tracking-wide">
        Keunggulan Jurusan
      </h1>
      <div class="flex justify-center flex-wrap py-20 space-y-10">
        <div class="flex justify-center gap-10 flex-wrap">
          <div
            v-for="(card, index) in cards"
            :key="index"
            ref="cardRefs"
            class="max-w-lg flex max-sm:flex-col gap-5 items-start py-5"
          >
            <img class="w-12" :src="card.src" alt="">
            <div class="space-y-3">
              <h1 class="text-lg text-white font-semibold">{{ card.title }}</h1>
              <p class="text-base text-white">{{ card.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>  
  </section>
</template>