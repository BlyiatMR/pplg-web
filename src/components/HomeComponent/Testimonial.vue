<script setup>
import { ref, computed, onMounted, onUnmounted, nextTick } from 'vue'
import { gsap } from 'gsap'

const testimonials = [
  {
    name: "Emil Kusmayadi",
    year: "Alumni Tahun 2024",
    img: "/src/assets/images/alumni.jpg",
    text: "Belajar di PPLG membuka peluang saya berkembang di dunia teknologi!",
  },
  {
    name: "Muhammad Hafizh",
    year: "Alumni Tahun 2025",
    img: "/src/assets/images/hafizh.jpg",
    text: "Belajar di PPLG membuka peluang saya berkembang di dunia teknologi!",
  },
  {
    name: "Rizky Ramadhan",
    year: "Alumni Tahun 2023",
    img: "/src/assets/images/rizky.jpg",
    text: "Pengalaman di PPLG sangat berharga dan membentuk karir saya di bidang IT.",
  },
  {
    name: "Siti Nurhaliza",
    year: "Alumni Tahun 2022",
    img: "/src/assets/images/siti.jpg",
    text: "PPLG memberikan saya banyak ilmu dan relasi di dunia teknologi.",
  },
]

const current = ref(0)
const cardRefs = ref([])

const visibleTestimonials = computed(() => {
  // Ambil 2 card, looping jika sudah di akhir array
  const arr = []
  for (let i = 0; i < 2; i++) {
    arr.push(testimonials[(current.value + i) % testimonials.length])
  }
  return arr
})

function animateCards() {
  nextTick(() => {
    cardRefs.value.forEach((el, i) => {
      if (!el) return
      gsap.fromTo(
        el,
        { opacity: 0, y: 40 },
        { opacity: 1, y: 0, duration: 0.6, ease: "power2.out" }
      )
    })
  })
}

let intervalId = null
onMounted(() => {
  animateCards()
  intervalId = setInterval(() => {
    current.value = (current.value + 1) % testimonials.length
    animateCards()
  }, 3500)
})
onUnmounted(() => {
  clearInterval(intervalId)
})
</script>

<template>
  <section class="bg-slate-50">
    <div class="max-w-[1100px] flex justify-between flex-wrap items-center max-xl:gap-10 mx-auto max-xl:mx-5 py-20">
      <div class="max-w-xs relative">
        <h1 class="font-semibold sm:text-4xl text-3xl text-slate-800 tracking-wide leading-tight">
          Cerita dari Alumni PPLG
        </h1>
        <p class="text-base font-medium text-slate-600 mt-5">
          Alumni kami telah membuktikan bahwa dengan semangat belajar dan ilmu yang bermanfaat.
        </p>
      </div>
      <div class="flex gap-10 flex-wrap">
        <div
          v-for="(item, idx) in visibleTestimonials"
          :key="item.name"
          ref="cardRefs"
          class="sm:max-w-xs max-w-full space-y-5 border border-slate-200 shadow-xl rounded-3xl py-10 px-7 bg-white transition-all duration-300"
        >
          <div class="rounded-full bg-[#7743DB] w-fit px-4 py-4">
            <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
              <path fill="#fff" d="M6.848 2.47a1 1 0 0 1-.318 1.378A7.3 7.3 0 0 0 3.75 7.01A3 3 0 1 1 1 10v-.027a4 4 0 0 1 .01-.232c.009-.15.027-.36.062-.618c.07-.513.207-1.22.484-2.014c.552-1.59 1.67-3.555 3.914-4.957a1 1 0 0 1 1.378.318m7 0a1 1 0 0 1-.318 1.378a7.3 7.3 0 0 0-2.78 3.162A3 3 0 1 1 8 10v-.027a4 4 0 0 1 .01-.232c.009-.15.027-.36.062-.618c.07-.513.207-1.22.484-2.014c.552-1.59 1.67-3.555 3.914-4.957a1 1 0 0 1 1.378.318"/>
            </svg>
          </div>
          <p class="text-base font-medium text-slate-600">
            {{ item.text }}
          </p>
          <div class="flex items-center gap-5 justify-center">
            <img class="w-12 h-12 object-cover rounded-full" :src="item.img" :alt="item.name">
            <div>
              <h1 class="text-lg font-semibold text-slate-800">{{ item.name }}</h1>
              <p>{{ item.year }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>