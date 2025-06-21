<script setup>
import { ref } from 'vue'
defineProps(['displayedImages', 'filteredImages', 'showAll', 'showMore', 'showLess', 'activeCategory'])
</script>

<template>
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
          :alt="img.desc"/>
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
      class="bg-[#926cd9] text-white px-6 py-2 rounded-lg font-semibold hover:bg-[#7743DB] transition">
      Lihat Semua Gambar
    </button>
  </div>
  <div v-if="filteredImages.length > 3 && showAll[activeCategory]" class="flex justify-center mt-4">
    <button
      @click="showLess"
      class="bg-slate-200 text-slate-700 px-6 py-2 rounded-lg font-semibold hover:bg-slate-300 transition"
    >
      Tampilkan Lebih Sedikit
    </button>
  </div>
</template>