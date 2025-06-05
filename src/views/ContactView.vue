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
        <div class="max-w-[1100px] mx-auto max-xl:mx-5">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Kontak Jurusan</h1>
            <div class="mx-auto text-center">
              <a class="text-base font-medium text-white text-center">Beranda > Kontak</a>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1100px] mx-auto max-xl:mx-5 flex">
          <div class="max-w-4xl mx-auto border border-slate-200 shadow-xl py-20 sm:px-16 px-8 rounded-3xl">
            <h1 class="sm:text-4xl text-3xl text-center text-slate-800 font-semibold tracking-wide"><span class="text-[#7743DB]">Hubungi</span>Kami</h1>
            <p class="text-base font-medium mt-5 text-slate-600 text-center">Jika Anda memiliki pertanyaan atau ingin mendapatkan informasi lebih lanjut tentang Jurusan PPLG, silakan hubungi kami melalui formulir di bawah ini.</p>
            <form action="" class="mt-5">
              <div class="grid sm:grid-cols-2 grid-cols-1 sm:gap-5 gap-2">
                <div>
                  <input id="username" type="text" placeholder="Nama*" class="text-gray-700/80 block w-full py-2 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg" fdprocessedid="79mp4">
                </div>
                <div>
                  <input type="email" placeholder="Email*" class="text-gray-700/80 block w-full py-2 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg" fdprocessedid="79mp4">
                </div>
              </div>
              <div class="mt-4">
                <input type="text" placeholder="Subjek Pertanyaan*" class="text-gray-700/80 block w-full py-2 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg">
              </div>
              <div>
                <textarea id="textarea" type="textarea" placeholder="Deskripsi" class="text-gray-700/80 block w-full py-5 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg h-32"></textarea>
              </div>
              <div class="mt-10 flex justify-center">
                <a href="#" class="flex w-fit justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-semibold hover:w-32 duration-300">Kirim <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
              </div>
            </form>
          </div>
        </div>
      </section>

      <Faq />

      <Cta />

      <Footer />
      </div>
  </main>
</template>