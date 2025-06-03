<script setup>
import Navbar from '@/components/Navbar.vue';
import Cta from '@/components/Cta.vue';
import Faq from '@/components/Faq.vue';
import Footer from '@/components/Footer.vue';

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
        <div class="max-w-[1280px] mx-auto max-xl:mx-5">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-24 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Galeri Jurusan</h1>
            <div class="mx-auto text-center">
              <a class="text-base font-medium text-white text-center">Beranda > Galeri</a>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1280px] mx-auto max-xl:mx-5">
            
        </div>
      </section>

      <Faq />

      <Cta />

      <Footer />
      </div>
  </main>
</template>