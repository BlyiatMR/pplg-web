<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'
import Navbar from '@/components/Navbar.vue'
import Cta from '@/components/Cta.vue'
import Footer from '@/components/Footer.vue'
import { Fancybox } from "@fancyapps/ui"
import "@fancyapps/ui/dist/fancybox/fancybox.css"

const categories = [
  { label: "Semua", value: "all" },
  { label: "Praktikum", value: "praktikum" },
  { label: "Lomba", value: "lomba" },
  { label: "Kunjungan", value: "kunjungan" },
  { label: "Workshop", value: "workshop" }
]

const images = [
  {
    src: "/src/assets/images/gallery/gallery-1.jpeg",
    desc: "Kegiatan Praktikum Siswa PPLG di Lab Komputer.",
    category: "praktikum"
  },
  {
    src: "/src/assets/images/gallery/gallery-2.jpeg",
    desc: "Perwakilan Jurusan PPLG Mengikuti Lomba Web Design di PNUP.",
    category: "lomba"
  },
  {
    src: "/src/assets/images/gallery/gallery-3.jpeg",
    desc: "Kunjungan industri ke perusahaan teknologi.",
    category: "lomba"
  },
  {
    src: "/src/assets/images/gallery/gallery-4.jpeg",
    desc: "Angkatan 55 Melakukan Kegiatan Kunjungan industri ke perusahaan teknologi.",
    category: "kunjungan"
  }
]

const activeCategory = ref("all")

const filteredImages = computed(() => {
  if (activeCategory.value === "all") return images
  return images.filter(img => img.category === activeCategory.value)
})

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
      <div class="w-[65rem] h-[65rem] max-2xl:w-[55rem] bg-white rounded-full absolute -left-[30rem] opacity-10 -z-50"></div>
      <div class="w-[75rem] h-[75rem] bg-white rounded-full absolute -top-[5rem] -left-[30rem] opacity-10 -z-50"></div>
      <div class="w-[55rem] h-[55rem] border border-white rounded-full absolute top-20 -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[75rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[30rem] opacity-10 -z-50"></div>

      <Navbar />

      <section class="z-50">
        <div class="max-w-[1100px] mx-auto max-xl:mx-5">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Galeri Jurusan</h1>
            <div class="mx-auto text-center">
              <a class="text-base font-medium text-white text-center">Beranda &gt; Galeri</a>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1100px] mx-auto max-xl:mx-5">
          <div>
            <nav>
              <ul class="flex flex-wrap sm:justify-center justify-start sm:gap-8 gap-y-5 gap-x-7">
                <li v-for="cat in categories" :key="cat.value">
                  <button
                    class="text-base font-semibold px-3 py-2 rounded-md transition-colors"
                    :class="activeCategory === cat.value
                      ? 'bg-[#926cd9] text-white'
                      : 'text-slate-800 hover:bg-[#926cd9] hover:text-white'"
                    @click="activeCategory = cat.value"
                  >
                    {{ cat.label }}
                  </button>
                </li>
              </ul>
            </nav>
          </div>
          <div class="mt-10 flex flex-wrap justify-center gap-5">
            <a
              v-for="img in filteredImages"
              :key="img.src"
              :href="img.src"
              data-fancybox="gallery"
              :data-caption="img.desc"
              class="block"
              style="outline:none"
            >
              <img
                class="w-80 h-80 object-cover rounded-3xl cursor-pointer transition shadow-xl"
                :src="img.src"
                :alt="img.desc"
              />
            </a>
            <div v-if="filteredImages.length === 0" class="text-slate-500 text-center w-full py-10">
              Tidak ada gambar pada kategori ini.
            </div>
          </div>
        </div>
      </section>

      <Cta />
      <Footer />
    </div>
  </main>
</template>