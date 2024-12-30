<script setup>
import Navbar from '@/components/Navbar.vue';

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

      <section class="h-[50rem] z-50">
        <div class="max-w-[1280px] mx-auto max-xl:mx-5 pt-10">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-24 py-20">
            <h1 id="title" class="sm:text-6xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Pengembangan Perangkat Lunak dan Game</h1>
          </div>
          <div class="pt-20">
            <img class="rounded-3xl object-cover object-top w-full h-[40rem]" src="/src/assets/images/class.jpg" alt="">
          </div>
        </div>
          <!-- <div class="flex pt-20">
            <div class="max-w-fit p-5 bg-[#9167E2] rounded-xl h-fit">
              <img class="rounded-lg w-96" src="/src/assets/images/pict-1.jpg" alt="">
            </div>
          </div> -->
        </section>

        <section class="h-screen bg-white">

        </section>
      </div>
  </main>
</template>