<script setup>
import BgCircles from '@/components/BgCircles.vue'
import Navbar from '@/components/Navbar.vue'
import Cta from '@/components/Cta.vue'
import Footer from '@/components/Footer.vue'
import InnerPageHero from '@/components/InnerPageHero.vue'
import OrganizationIntro from '@/components/OrganizationComponent/OrganizationIntro.vue'
import OrganizationWorkCarousel from '@/components/OrganizationComponent/OrganizationWorkCarousel.vue'
import OrganizationJoinSection from '@/components/OrganizationComponent/OrganizationJoinSection.vue'
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">
      <BgCircles />

      <Navbar />

      <InnerPageHero title="Ekstrakurikuler Jurusan" breadcrumb="Ekstrakurikuler" />

      <OrganizationHero />

      <OrganizationIntro />

      <OrganizationWorkCarousel :work="work" />

      <OrganizationJoinSection />

      <Cta />
      
      <Footer />
    </div>
  </main>
</template>

<script>
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
</script>