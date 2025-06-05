<template>
  <section class="bg-slate-50">
    <div class="max-w-[1100px] max-xl:gap-10 mx-auto max-xl:mx-5 py-20">
      <h1 class="font-semibold text-center sm:text-4xl text-3xl text-slate-800 tracking-wide">
        Pertanyaan yang Sering Diajukan
      </h1>
      <div class="mt-10 flex flex-wrap justify-center gap-5">
        <div
          class="space-y-5"
          v-for="(faq, i) in faqs"
          :key="i">
          <div class="max-w-lg bg-white rounded-xl mx-auto shadow-xl sm:px-10 px-6 py-5">
            <h3
              @click="toggleFaq(i)"
              class="font-semibold text-slate-800 sm:text-lg text-base cursor-pointer flex justify-between items-center tracking-wide">
              {{ faq.question }}
              <span
                :class="openIndex === i ? 'rotate-180' : ''"
                class="transition-transform">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m17 14l-5-5m0 0l-5 5"/></svg></span>
            </h3>
            <div
              class="overflow-hidden transition-all duration-300"
              :ref="el => answerRefs[i] = el"
              :style="{ height: openIndex === i ? contentHeights[i] + 'px' : '0px' }">
              <p class="text-base font-medium text-slate-600 mt-3">
                {{ faq.answer }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted, nextTick, watch } from 'vue'

const faqs = ref([
  {
    question: 'Apa itu jurusan PPLG?',
    answer:
      'PPLG adalah singkatan dari Pengembangan Perangkat Lunak dan Gim, jurusan yang fokus pada pembuatan aplikasi, website, hingga game. Di sini kamu belajar coding, desain antarmuka, dan pengembangan software dari nol.',
  },
  {
    question: 'Apakah jurusan ini cocok untuk yang suka main game?',
    answer:
      'Kalau kamu suka main game dan penasaran bagaimana game dibuat, jurusan ini bisa jadi pilihan tepat. Kamu bisa belajar membuat game sendiri, baik 2D maupun 3D.',
  },
  {
    question: 'Apa manfaat memilih jurusan PPLG untuk masa depan?',
    answer:
      'Lulus di Jurusan ini akan sangat dibutuhkan di era industri 4.0. Di masa yang akan datang, hampir semua bidang membutuhkan teknologi, sehingga kamu memiliki peluang besar dalam dunia kerja, startup, hingga karier global.',
  },
  {
    question: 'Apakah harus jago bermain komputer/laptop sebelum masuk PPLG?',
    answer:
      'Tidak perlu. Yang penting kamu punya minat belajar teknologi dan mau terus berkembang. Semua akan diajarkan dari dasar oleh guru-guru.',
  },
  {
    question: 'Apakah bisa membuat aplikasi seperti Instagram atau TikTok?',
    answer:
      'Kalau kamu sudah paham dasar pembuatan aplikasi mobile dan website. Dengan latihan dan pengalaman, kamu berpotensi membuat aplikasi serupa di masa depan.',
  },
  {
    question: 'Apa bedanya PPLG dengan TKJ (Teknik Komputer dan Jaringan)?',
    answer:
      'PPLG fokus pada pengembangan perangkat lunak (software) dan pembuatan game/aplikasi. Sementara TKJ lebih fokus ke perangkat keras (hardware) dan pengelolaan jaringan komputer.',
  },
])

const openIndex = ref(null)
const answerRefs = []
const contentHeights = ref([])

const calculateHeights = async () => {
  await nextTick()
  contentHeights.value = answerRefs.map((el) => el?.scrollHeight || 0)
}

const toggleFaq = async (index) => {
  openIndex.value = openIndex.value === index ? null : index
}

onMounted(() => {
  calculateHeights()
  window.addEventListener('resize', calculateHeights)
})

onUnmounted(() => {
  window.removeEventListener('resize', calculateHeights)
})

watch(openIndex, async () => {
  await calculateHeights()
})
</script>