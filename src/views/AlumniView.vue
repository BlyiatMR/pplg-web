<script setup>
import BgCircles from '@/components/BgCircles.vue'
import Navbar from '@/components/Navbar.vue'
import Cta from '@/components/Cta.vue'
import Footer from '@/components/Footer.vue'
import InnerPageHero from '@/components/InnerPageHero.vue'
import AlumniList from '@/components/AlumniComponent/AlumniList.vue'
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">
      <BgCircles />

      <Navbar />

      <InnerPageHero title="Alumni Jurusan" breadcrumb="Alumni" />

      <AlumniList />

      <Cta />

      <Footer />
    </div>
  </main>
</template>