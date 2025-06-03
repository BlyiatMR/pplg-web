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
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Alumni Jurusan</h1>
            <div class="mx-auto text-center">
              <a class="text-base font-medium text-white text-center">Beranda > Alumni</a>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1280px] mx-auto max-xl:mx-5">
          <div class="flex flex-wrap sm:gap-10 gap-5 justify-center">
            <div class="max-w-fit flex gap-3 bg-yellow-400 rounded-3xl p-12 shadow-2xl hover:-translate-y-2 duration-300 cursor-pointer">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="text-slate-800" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="m19 5l-7-3l-7 3l3.5 1.5v2S9.667 8 12 8s3.5.5 3.5.5v-2zm0 0v4m-3.5-.5v1a3.5 3.5 0 1 1-7 0v-1m-.717 8.203c-1.1.685-3.986 2.082-2.229 3.831C6.413 21.39 7.37 22 8.571 22h6.858c1.202 0 2.158-.611 3.017-1.466c1.757-1.749-1.128-3.146-2.229-3.83a7.99 7.99 0 0 0-8.434 0" color="currentColor"/></svg>
              <h3 class="text-lg font-semibold text-slate-800">
                Alumni 2021</h3>
            </div>
            <div class="max-w-fit flex gap-3 bg-yellow-400 rounded-3xl p-12 shadow-2xl hover:-translate-y-2 duration-300 cursor-pointer">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="text-slate-800" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="m19 5l-7-3l-7 3l3.5 1.5v2S9.667 8 12 8s3.5.5 3.5.5v-2zm0 0v4m-3.5-.5v1a3.5 3.5 0 1 1-7 0v-1m-.717 8.203c-1.1.685-3.986 2.082-2.229 3.831C6.413 21.39 7.37 22 8.571 22h6.858c1.202 0 2.158-.611 3.017-1.466c1.757-1.749-1.128-3.146-2.229-3.83a7.99 7.99 0 0 0-8.434 0" color="currentColor"/></svg>
              <h3 class="text-lg font-semibold text-slate-800">
                Alumni 2022</h3>
            </div>
            <div class="max-w-fit flex gap-3 bg-yellow-400 rounded-3xl p-12 shadow-2xl hover:-translate-y-2 duration-300 cursor-pointer">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="text-slate-800" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="m19 5l-7-3l-7 3l3.5 1.5v2S9.667 8 12 8s3.5.5 3.5.5v-2zm0 0v4m-3.5-.5v1a3.5 3.5 0 1 1-7 0v-1m-.717 8.203c-1.1.685-3.986 2.082-2.229 3.831C6.413 21.39 7.37 22 8.571 22h6.858c1.202 0 2.158-.611 3.017-1.466c1.757-1.749-1.128-3.146-2.229-3.83a7.99 7.99 0 0 0-8.434 0" color="currentColor"/></svg>
              <h3 class="text-lg font-semibold text-slate-800">
                Alumni 2023</h3>
            </div>
            <div class="max-w-fit flex gap-3 bg-yellow-400 rounded-3xl p-12 shadow-2xl hover:-translate-y-2 duration-300 cursor-pointer">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="text-slate-800" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="m19 5l-7-3l-7 3l3.5 1.5v2S9.667 8 12 8s3.5.5 3.5.5v-2zm0 0v4m-3.5-.5v1a3.5 3.5 0 1 1-7 0v-1m-.717 8.203c-1.1.685-3.986 2.082-2.229 3.831C6.413 21.39 7.37 22 8.571 22h6.858c1.202 0 2.158-.611 3.017-1.466c1.757-1.749-1.128-3.146-2.229-3.83a7.99 7.99 0 0 0-8.434 0" color="currentColor"/></svg>
              <h3 class="text-lg font-semibold text-slate-800">
                Alumni 2024</h3>
            </div>
            <div class="max-w-fit flex gap-3 bg-yellow-400 rounded-3xl p-12 shadow-2xl hover:-translate-y-2 duration-300 cursor-pointer">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="text-slate-800" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="m19 5l-7-3l-7 3l3.5 1.5v2S9.667 8 12 8s3.5.5 3.5.5v-2zm0 0v4m-3.5-.5v1a3.5 3.5 0 1 1-7 0v-1m-.717 8.203c-1.1.685-3.986 2.082-2.229 3.831C6.413 21.39 7.37 22 8.571 22h6.858c1.202 0 2.158-.611 3.017-1.466c1.757-1.749-1.128-3.146-2.229-3.83a7.99 7.99 0 0 0-8.434 0" color="currentColor"/></svg>
              <h3 class="text-lg font-semibold text-slate-800">
                Alumni 2025</h3>
            </div>
          </div>
        </div>
      </section>

      <Faq />

      <Cta />

      <Footer />
      </div>
  </main>
</template>