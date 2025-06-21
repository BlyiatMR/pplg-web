<script setup>
import BgCircles from '@/components/BgCircles.vue'
import Navbar from '@/components/Navbar.vue'
import Cta from '@/components/Cta.vue'
import Footer from '@/components/Footer.vue'
import InnerPageHero from '@/components/InnerPageHero.vue'
import GalleryCategoryNav from '@/components/GalleryComponent/GalleryCategoryNav.vue'
import GalleryGrid from '@/components/GalleryComponent/GalleryGrid.vue'
import { ref, computed, onMounted, onUnmounted } from 'vue'
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

      <InnerPageHero title="Galeri Jurusan" breadcrumb="Galeri" />

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
          <GalleryCategoryNav
            :categories="categories"
            :activeCategory="activeCategory"
            @update:activeCategory="val => activeCategory = val"
          />
          <GalleryGrid
            :displayedImages="displayedImages"
            :filteredImages="filteredImages"
            :showAll="showAll"
            :showMore="showMore"
            :showLess="showLess"
            :activeCategory="activeCategory"
          />
        </div>
      </section>

      <Cta />

      <Footer />
    </div>
  </main>
</template>

<script>
const images = [
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