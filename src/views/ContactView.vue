<script setup>
import BgCircles from '@/components/BgCircles.vue'
import Navbar from '@/components/Navbar.vue'
import Cta from '@/components/Cta.vue'
import Footer from '@/components/Footer.vue'
import InnerPageHero from '@/components/InnerPageHero.vue'
import ContactInfo from '@/components/ContactComponent/ContactInfo.vue'
import ContactForm from '@/components/ContactComponent/ContactForm.vue'
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">
      <BgCircles />

      <Navbar />

      <InnerPageHero title="Kontak Jurusan" breadcrumb="Kontak" />

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5 flex flex-wrap justify-around items-center gap-10">
          <ContactInfo />
          <ContactForm />
        </div>
      </section>

      <Cta />

      <Footer />
    </div>
  </main>
</template>