<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'
import BgCircles from '@/components/BgCircles.vue';
import Navbar from '@/components/Navbar.vue'
import Cta from '@/components/Cta.vue'
import Footer from '@/components/Footer.vue'
import { Fancybox } from "@fancyapps/ui"
import "@fancyapps/ui/dist/fancybox/fancybox.css"

const categories = [
  { label: "Praktikum", value: "praktikum" },
  { label: "Lomba", value: "lomba" },
  { label: "Kunjungan", value: "kunjungan" },
  { label: "Workshop", value: "workshop" }
]

const activeCategory = ref(categories[0].value)
const showAll = ref({})

const filteredImages = computed(() => {
  return images.filter(img => img.category === activeCategory.value)
})

const displayedImages = computed(() => {
  const imgs = filteredImages.value
  return showAll.value[activeCategory.value] ? imgs : imgs.slice(0, 3)
})

function showMore() {
  showAll.value = { ...showAll.value, [activeCategory.value]: true }
}
function showLess() {
  showAll.value = { ...showAll.value, [activeCategory.value]: false }
}

onMounted(() => {
  Fancybox.bind('[data-fancybox="gallery"]')
})

onUnmounted(() => {
  Fancybox.destroy()
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
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Galeri Jurusan</h1>
            <div class="mx-auto text-center">
              <p class="text-base font-medium text-white"><a href="/" class="mr-3">Beranda</a> <span class="mr-3 text-gray-300">/</span> Galeri</p>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
          <div>
            <nav>
              <ul class="flex flex-wrap sm:justify-center justify-start sm:gap-8 gap-y-2 gap-x-7">
                <li v-for="cat in categories" :key="cat.value">
                  <button
                    class="text-base font-semibold px-3 py-2 rounded-md transition-colors"
                    :class="activeCategory === cat.value
                      ? 'bg-[#926cd9] text-white'
                      : 'text-slate-800 hover:bg-[#926cd9] hover:text-white'"
                    @click="activeCategory = cat.value">
                    {{ cat.label }}
                  </button>
                </li>
              </ul>
            </nav>
          </div>
          <div class="mt-10 flex flex-wrap justify-center gap-5">
            <a
              v-for="img in displayedImages"
              :key="img.src"
              :href="img.src"
              data-fancybox="gallery"
              :data-caption="img.desc"
              class="block"
              style="outline:none">
              <div class="relative w-80 h-80">
                <img
                  class="w-80 h-80 object-cover bg-primary rounded-3xl border-t-[6px] border-[#B79FEB] cursor-pointer transition shadow-xl"
                  :src="img.src"
                  :alt="img.desc"
                />
                <div class="absolute bottom-0 left-0 right-0 bg-black/60 text-white text-xs px-4 py-2 rounded-b-3xl">
                  <span class="block">{{ img.desc }}</span>
                  <span class="block mt-1">Upload: {{ new Date(img.date).toLocaleDateString('id-ID', { day: '2-digit', month: 'long', year: 'numeric' }) }}</span>
                </div>
              </div>
            </a>
            <div v-if="filteredImages.length === 0" class="text-slate-500 text-center w-full py-10">
              Tidak ada gambar pada kategori ini.
            </div>
          </div>
          <div v-if="filteredImages.length > 3 && !showAll[activeCategory]" class="flex justify-center mt-8">
            <button
              @click="showMore"
              class="bg-yellow-400 text-slate-800 px-6 py-2 rounded-lg font-semibold hover:bg-yellow-400 transition">
              Lihat Semua Gambar
            </button>
          </div>
          <div v-if="filteredImages.length > 3 && showAll[activeCategory]" class="flex justify-center mt-4">
            <button
              @click="showLess"
              class="bg-slate-200 text-slate-700 px-6 py-2 rounded-lg font-semibold hover:bg-slate-300 transition">
              Tampilkan Lebih Sedikit
            </button>
          </div>
        </div>
      </section>

      <Cta />
      <Footer />
    </div>
  </main>
</template>

<script>
export const images = [
  {
    src: new URL('@/assets/images/gallery/gallery-7.jpeg', import.meta.url).href,
    desc: "Angkatan 5 PPLG Melakukan Kegiatan Kunjungan industri ke PT. Rupa Raya Indonesia.",
    category: "kunjungan",
    date: "2024-06-01"
  },
  {
    src: new URL('@/assets/images/gallery/gallery-5.jpeg', import.meta.url).href,
    desc: "Siswa PPLG Angkatan 5 bersiap di meja lomba dengan perlengkapan yang disediakan panitia.",
    category: "lomba",
    date: "2024-05-28"
  },
  {
    src: new URL('@/assets/images/gallery/gallery-6.jpeg', import.meta.url).href,
    desc: "Siswa Angkatan 5 PPLG Mengikuti Lomba Web Development di SMK Telkom Makassar.",
    category: "lomba",
    date: "2024-05-20"
  },
  {
    src: new URL('@/assets/images/gallery/gallery-1.jpeg', import.meta.url).href,
    desc: "Kegiatan Praktikum Siswa PPLG di Lab Komputer.",
    category: "praktikum",
    date: "2024-05-15"
  },
  {
    src: new URL('@/assets/images/gallery/gallery-8.jpeg', import.meta.url).href,
    desc: "Proses Development Website oleh Siswa PPLG Angkatan 4 dalam Lomba Web Design.",
    category: "lomba",
    date: "2024-05-10"
  },
  {
    src: new URL('@/assets/images/gallery/gallery-2.jpeg', import.meta.url).href,
    desc: "3 Siswa Angkatan 4 PPLG Mengikuti Lomba Web Design di PNUP.",
    category: "lomba",
    date: "2024-05-05"
  },
  {
    src: new URL('@/assets/images/gallery/gallery-4.jpeg', import.meta.url).href,
    desc: "Angkatan 4 PPLG Melakukan Kegiatan Kunjungan industri ke PT. Yuscorp.",
    category: "kunjungan",
    date: "2024-04-28"
  }
]
</script>