<script setup>
import NavbarVue from '@/components/Navbar.vue';

</script>
<script>
export default {
  name: 'HomeView',
};
</script>

<template>
  <main>

    <div class="relative overflow-hidden z-50">
      
      <div class="w-[65rem] h-[65rem] max-2xl:w-[55rem] bg-white rounded-full absolute -left-[30rem] opacity-10 -z-50"></div>
      <div class="w-[75rem] h-[75rem] bg-white rounded-full absolute -top-[5rem] -left-[30rem] opacity-10 -z-50"></div>

      <div class="w-[55rem] h-[55rem] border border-white rounded-full absolute top-20 -right-[30rem] opacity-25 -z-50"></div>
      <div class="w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[30rem] opacity-25 -z-50"></div>
      <div class="w-[75rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[30rem] opacity-25 -z-50"></div>

      <NavbarVue />

      <section class="max-w-[1440px] flex px-28 z-50 h-[42rem] mt-10">
        <div class="max-w-2xl space-y-5 pt-24">
          <h1 class="text-6xl text-white font-semibold tracking-wide leading-tight">Pengembangan Perangkat Lunak dan Game</h1>
          <h3 class="text-base text-white tracking-wide">Jurusan IT Kekinian Menjadi Ahli Teknologi Masa Depan Pembelajaran yang berfokus pada tren teknologi terkini dan praktik industri</h3>
          <div class="flex pt-10 gap-10">
            <a href="#" class="flex w-[270px] justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-medium">Jelajahi Jurusan PPLG <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
            <a href="#" class="flex items-center gap-3 text-white tracking-wide"><svg class="w-10 bg-yellow-400 p-2 rounded-full" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path class="fill-black" d="M21.409 9.353a2.998 2.998 0 0 1 0 5.294L8.597 21.614C6.534 22.737 4 21.277 4 18.968V5.033c0-2.31 2.534-3.769 4.597-2.648z"/></svg> Yuk Intip Aktivitas Jurusan</a>
          </div>
        </div>
        <div class="flex">
          <img class="w-[40rem] absolute object-cover" src="/src/assets/images/boy.png" alt="">
          <img class="w-72 absolute object-cover" src="/src/assets/images/girl.png" alt="">
        </div>
        <!-- <div class="flex pt-20">
          <div class="max-w-fit p-5 bg-[#9167E2] rounded-xl h-fit">
            <img class="rounded-lg w-96" src="/src/assets/images/pict-1.jpg" alt="">
          </div>
        </div> -->
      </section>

      <section class="h-screen bg-slate-50 rounded-tr-[15rem] rounded-tl-[15rem] py-20">
        <div class="max-w-[1440px] relative mx-auto space-y-10">
          <div class="absolute right-20 w-20 h-20 bg-[#7743DB] rounded-full opacity-10"></div>
          <div class="absolute top-20 left-0 w-20 h-20 border-[10px] border-[#7743DB] rounded-full opacity-10"></div>
          <div class="absolute bottom-0 right-0 w-16 h-16 bg-[#FFC53B] rounded-full opacity-10"></div>
          <h2 class="max-w-6xl mx-auto text-center font-semibold text-6xl text-slate-600 leading-tight">Jurusan PPLG fokus pada pembelajaran tentang bagaimana membuat, mengembangkan, dan mengelola Software Komputer</h2>
          <a href="#" class="flex mx-auto w-[210px] justify-between bg-[#7743DB] text-white py-2 px-5 rounded-lg tracking-wide font-medium">Lebih Lengkap <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
        </div>
      </section>

    </div>
  </main>
</template>
