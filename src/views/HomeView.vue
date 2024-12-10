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

      <section class="max-w-[1440px] mx-auto flex flex-wrap justify-between z-50 h-[42rem] mt-10">
        <div class="max-w-2xl space-y-5 pt-24">
          <h1 class="text-6xl text-white font-semibold tracking-wide leading-tight">Pengembangan Perangkat Lunak dan Game</h1>
          <h3 class="text-base text-white tracking-wide">Jurusan IT Kekinian Menjadi Ahli Teknologi Masa Depan Pembelajaran yang berfokus pada tren teknologi terkini dan praktik industri</h3>
          <div class="flex pt-10 gap-10">
            <a href="#" class="flex w-[270px] justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-medium">Jelajahi Jurusan PPLG <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
            <a href="#" class="flex items-center gap-3 text-white tracking-wide"><svg class="w-10 bg-yellow-400 p-2 rounded-full" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path class="fill-black" d="M21.409 9.353a2.998 2.998 0 0 1 0 5.294L8.597 21.614C6.534 22.737 4 21.277 4 18.968V5.033c0-2.31 2.534-3.769 4.597-2.648z"/></svg> Yuk Intip Aktivitas Jurusan</a>
          </div>
        </div>
        <div class="flex">
          <img class="w-[45rem] -z-50" src="/src/assets/images/actr.png" alt="">
        </div>
        <!-- <div class="flex pt-20">
          <div class="max-w-fit p-5 bg-[#9167E2] rounded-xl h-fit">
            <img class="rounded-lg w-96" src="/src/assets/images/pict-1.jpg" alt="">
          </div>
        </div> -->
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <!-- <div class="max-w-6xl flex items-center gap-40 mx-auto">
          <div>
            <img class="w-[20rem]" src="/src/assets/images/boy.png" alt="">
          </div>
          <div>
            <h1 class="font-semibold text-4xl text-slate-800">Selamat Datang di Jurusan PPLG</h1>
            <p class="max-w-5xl text-slate-600 text-base mt-5">Kami sangat bangga menyambut kalian di jurusan Pengembangan Perangkat Lunak dan Gim (PPLG), tempat kreativitas bertemu teknologi. Di sini, kalian akan belajar dan berkembang menjadi talenta muda yang siap menghadapi era digital. <br><br>Kami percaya, setiap langkah kecil yang kalian ambil di jurusan ini akan menjadi pijakan menuju mimpi besar. Jadi, mari manfaatkan setiap kesempatan untuk belajar, berinovasi, dan berkarya. <br><br>Selamat menikmati perjalanan belajar di PPLG! Jika ada tantangan, ingat, kalian tidak sendiri—kami ada untuk mendukung dan membimbing kalian. <br><br>Semangat berkarya, generasi hebat masa depan!</p>
          </div>
        </div> -->
        <div class="max-w-[1440px] relative mx-auto">
          <h2 class="max-w-7xl mx-auto text-center font-semibold text-6xl text-slate-600 leading-tight">.   .   .Jurusan sekolah yang fokus pada pembelajaran tentang bagaimana membuat, mengembangkan, dan mengelola Software Komputer.   .   .</h2>
        </div>
        <div class="relative max-w-7xl mx-auto flex gap-5 flex-wrap justify-around bg-[#7743DB] rounded-3xl py-10 px-5 z-50">

          <div class="w-60 h-60 rounded-full bg-white absolute -left-20 -top-20 opacity-10 -z-50"></div>
          <div class="w-80 h-80 rounded-full bg-white absolute -left-20 -top-20 opacity-10 -z-50"></div>
          <div class="w-60 h-60 rounded-full border absolute -right-20 -bottom-20 opacity-20 -z-50"></div>
          <div class="w-80 h-80 rounded-full border absolute -right-20 -bottom-20 opacity-20 -z-50"></div>
          <div class="w-[25rem] h-[25rem] rounded-full border absolute -right-20 -bottom-20 opacity-20 -z-50"></div>

          <div class="border-r">
            <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="none" class="stroke-white" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" color="currentColor"><path d="M20 14.5v-8c0-1.886 0-2.828-.586-3.414S17.886 2.5 16 2.5H8c-1.886 0-2.828 0-3.414.586S4 4.614 4 6.5v8m-.502 1.015L4.02 14.5h15.932l.55 1.015c1.443 2.662 1.803 3.993 1.254 4.989s-2.002.996-4.91.996H7.154c-2.909 0-4.363 0-4.911-.996c-.549-.996-.19-2.327 1.254-4.989"/><path d="m15.5 7l.92.793c.387.333.58.5.58.707s-.193.374-.58.707L15.5 10m-7-3l-.92.793c-.387.333-.58.5-.58.707s.193.374.58.707L8.5 10M13 6l-2 5"/></g></svg>
            <div class="mt-5">
              <h1 class="text-xl text-white font-semibold">Web Development</h1>
              <p class="w-72 mt-2 text-base text-white">Membuat website interaktif dengan teknologi modern.</p>
            </div>
          </div>
          <div class="border-r">
            <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16"><path class="fill-white" d="M11.5 4a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1zM11 6.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 0 1h-2a.5.5 0 0 1-.5-.5m.5 1.5a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1z"/><path class="fill-white" fill-rule="evenodd" d="M3 1C1.34 1 0 2.34 0 4v8c0 1.66 1.34 3 3 3h10c1.66 0 3-1.34 3-3V4c0-1.66-1.34-3-3-3zm10 1h-3v12h3c1.1 0 2-.895 2-2V4c0-1.1-.895-2-2-2M3 2h6v12H3c-1.1 0-2-.895-2-2V4c0-1.1.895-2 2-2" clip-rule="evenodd"/></svg>
            <div class="mt-5">
              <h1 class="text-xl text-white font-semibold">UI/UX</h1>
              <p class="w-72 mt-2 text-base text-white">Mendesain antarmuka menarik dan user-friendly.</p>
            </div>
          </div>
          <div class="border-r">
            <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="none" class="stroke-white" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 8c.01-2.644.108-4.059 1.024-4.975C7.049 2 8.699 2 11.999 2s4.95 0 5.975 1.025c.916.916 1.013 2.33 1.023 4.975M5 16c.01 2.644.108 4.059 1.024 4.975C7.049 22 8.699 22 11.999 22s4.95 0 5.975-1.025c.916-.916 1.013-2.33 1.023-4.975M11 19h2m3-9l1.227 1.057c.515.445.773.667.773.943s-.258.498-.773.943L16 14m-8-4l-1.227 1.057C6.258 11.502 6 11.724 6 12s.258.498.773.943L8 14m5-5l-2 6" color="currentColor"/></svg>
            <div class="mt-5">
              <h1 class="text-xl text-white font-semibold">Mobile Development</h1>
              <p class="w-72 mt-2 text-base text-white">Membangun aplikasi Android sesuai standar industri.</p>
            </div>
          </div>
          <div class="">
            <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 36 36"><path class="fill-white" d="M30.86 20.94a4.7 4.7 0 0 1 1.86.64h.05a15.1 15.1 0 0 0-.61-8.37a1 1 0 0 0-1.28-.59a1 1 0 0 0-.59 1.28a13.2 13.2 0 0 1 .57 7.04m-4.53 7.64a13 13 0 0 1-6.07 2.82a1 1 0 1 0 .17 2h.18a15.16 15.16 0 0 0 7.21-3.4v-.07a4.7 4.7 0 0 1-1.49-1.35m-10.71 2.76a13.2 13.2 0 0 1-4.29-1.61a15 15 0 0 1-1.63-1.11A4.7 4.7 0 0 1 8.24 30a16 16 0 0 0 2.07 1.48a15.4 15.4 0 0 0 4.94 1.86h.19a1 1 0 0 0 .18-2M4.56 21.15a4 4 0 0 0 .6-.09A13 13 0 0 1 5.7 14a1 1 0 0 0-1.88-.69a15 15 0 0 0-.56 8.43a4.8 4.8 0 0 1 1.3-.59"/><path class="fill-white" d="M31.9 23a3.2 3.2 0 0 0-2.43-.42a3.3 3.3 0 0 0-1.4.77l-3.87-2.24a6.87 6.87 0 0 0-2.77-8.43l-.11-.07a6.6 6.6 0 0 0-2.42-.81V8a3.22 3.22 0 0 0 1.88-1.5A3.3 3.3 0 0 0 19.65 2a3.15 3.15 0 0 0-2.42-.32a3.24 3.24 0 0 0-2 1.51a3.3 3.3 0 0 0 1.13 4.46a3 3 0 0 0 .74.35v3.8a6.64 6.64 0 0 0-4.86 3.28a6.85 6.85 0 0 0-.42 6l-4 2.29a4 4 0 0 0-.45-.34A3.2 3.2 0 0 0 3 24.21a3.3 3.3 0 0 0 1.1 4.46a3.2 3.2 0 0 0 1.65.46a3 3 0 0 0 .78-.1a3.24 3.24 0 0 0 2.29-4.11l3.88-2.24a7.1 7.1 0 0 0 1.89 1.71a6.49 6.49 0 0 0 8.73-1.7l3.83 2.21a3.29 3.29 0 0 0 1.45 3.64a3.15 3.15 0 0 0 1.64.46A3.17 3.17 0 0 0 33 27.41A3.3 3.3 0 0 0 31.9 23M7 26.62a1.4 1.4 0 0 1-.91.64A1.36 1.36 0 0 1 5 27.11a1.48 1.48 0 0 1-.5-2a1.4 1.4 0 0 1 .88-.66a1.3 1.3 0 0 1 .34-.05a1.4 1.4 0 0 1 .75.22a1.48 1.48 0 0 1 .53 2m9.78-22.53a1.4 1.4 0 0 1 .88-.66a1.3 1.3 0 0 1 .34-.05a1.4 1.4 0 0 1 .72.2a1.48 1.48 0 0 1 .5 2a1.4 1.4 0 0 1-.88.66a1.36 1.36 0 0 1-1.06-.15a1.48 1.48 0 0 1-.5-2m2.41 19.32a4.8 4.8 0 0 1-3.68-.54A5.07 5.07 0 0 1 13.78 16A4.88 4.88 0 0 1 18 13.57a4.8 4.8 0 0 1 2.46.67a5.07 5.07 0 0 1 1.73 6.87a4.86 4.86 0 0 1-3 2.3m12.25 3.08a1.45 1.45 0 0 1-.88.67A1.36 1.36 0 0 1 29.5 27a1.48 1.48 0 0 1-.5-2a1.4 1.4 0 0 1 .9-.72a2 2 0 0 1 .34 0a1.3 1.3 0 0 1 .69.19a1.48 1.48 0 0 1 .51 2.02M8.05 10a13 13 0 0 1 5.35-3.77a5 5 0 0 1-.17-2.07a15.15 15.15 0 0 0-6.7 4.51A1 1 0 0 0 8.05 10"/><path class="fill-white" d="M24.67 7.23A13.1 13.1 0 0 1 27.93 10a1 1 0 1 0 1.52-1.3a15 15 0 0 0-3.76-3.2a16 16 0 0 0-2.94-1.33a4.8 4.8 0 0 1-.15 2.06a14 14 0 0 1 2.07 1"/><path fill="none" d="M0 0h36v36H0z"/></svg>
            <div class="mt-5">
              <h1 class="text-xl text-white font-semibold">IoT</h1>
              <p class="w-72 mt-2 text-base text-white">Mengembangkan hardware dengan internet.</p>
            </div>
          </div>
        </div>
      </section>

      <section class="">
        <div class="max-w-[1440px] relative mx-auto py-20">
          <h1 class="max-w-7xl mx-auto text-center font-semibold text-6xl text-white leading-tight">Kenapa Memilih Jurusan PPLG?</h1>
          <div class="flex justify-center flex-wrap py-20 space-y-10">
            <div class="flex gap-10">
              <div class="max-w-xl flex gap-5 items-start">
                <svg class="w-40" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48"><g fill="none" class="stroke-white" stroke-linejoin="round" stroke-width="4"><path stroke-linecap="round" d="M24 6C14.059 6 6 14.059 6 24s8.059 18 18 18s18-8.059 18-18"/><path stroke-linecap="round" d="M24 15a9 9 0 1 0 9 9m-9 0l6.3-6.306"/><path fill="currentColor" d="M30.3 11.426V17.7h6.325L42 12.3h-6.297V6z"/></g></svg>
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Kurikulum Up-to-date</h1>
                  <p class="text-base text-white">Kurikulum dirancang agar sejalan dengan perkembangan teknologi terkini, menjadikan siswa siap bersaing di pasar kerja.</p>
                </div>
              </div>
              <div class="max-w-xl flex gap-5 items-start">
                <svg class="w-32" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path class="fill-white" d="M2 5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2h-7v2h3a1 1 0 1 1 0 2H8a1 1 0 1 1 0-2h3v-2H4a2 2 0 0 1-2-2zm18 11V5H4v11z"/></svg>
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Fasilitas Komputer</h1>
                  <p class="text-base text-white">Dilengkapi fasilitas komputer terkini dan software terbaru untuk mendukung pembelajaran maksimal.</p>
                </div>
              </div>
            </div>
            <div class="flex gap-10">
              <div class="max-w-xl flex gap-5 items-start">
                <svg class="w-32" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="none" class="stroke-white" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" color="currentColor"><path d="M11.007 21H9.605c-3.585 0-5.377 0-6.491-1.135S2 16.903 2 13.25s0-5.48 1.114-6.615S6.02 5.5 9.605 5.5h3.803c3.585 0 5.378 0 6.492 1.135c.857.873 1.054 2.156 1.1 4.365"/><path d="M17.111 13.255c.185-.17.277-.255.389-.255s.204.085.389.255l.713.657c.086.079.129.119.182.138c.054.02.112.018.23.013l.962-.038c.248-.01.372-.014.457.057s.102.194.135.44l.132.986c.016.114.023.17.051.22c.028.048.073.083.163.154l.776.61c.192.152.288.227.307.335s-.046.212-.174.42l-.526.847c-.06.097-.09.146-.1.2s.002.111.026.223l.209.978c.05.24.076.36.021.456s-.172.134-.405.21l-.926.301c-.11.036-.166.054-.209.09c-.043.037-.07.089-.123.192l-.452.871c-.115.223-.173.334-.278.372s-.22-.01-.452-.106l-.888-.368c-.109-.045-.163-.068-.22-.068s-.111.023-.22.068l-.888.368c-.232.096-.347.144-.452.106s-.163-.15-.278-.372l-.452-.871c-.054-.103-.08-.155-.123-.191s-.099-.055-.209-.09l-.926-.302c-.233-.076-.35-.114-.405-.21s-.03-.215.021-.456l.21-.978c.023-.112.035-.168.025-.222a.6.6 0 0 0-.1-.2l-.525-.848c-.13-.208-.194-.312-.175-.42s.115-.183.307-.334l.776-.61c.09-.072.135-.107.163-.156s.035-.105.05-.22l.133-.985c.033-.245.05-.369.135-.44s.209-.067.457-.057l.963.038c.117.005.175.007.229-.013c.053-.02.096-.059.182-.138zM16 5.5l-.1-.31c-.495-1.54-.742-2.31-1.331-2.75C13.979 2 13.197 2 11.63 2h-.263c-1.565 0-2.348 0-2.937.44c-.59.44-.837 1.21-1.332 2.75L7 5.5"/></g></svg>
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Peluang Karir Luas</h1>
                  <p class="text-base text-white">Jurusan ini membuka jalan untuk berbagai profesi seperti web developer, mobile developer, UI/UX designer, atau pengembang IoT.</p>
                </div>
              </div>
              <div class="max-w-xl flex gap-5 items-start">
                <svg class="w-32" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path class="fill-white" d="M8.75 7a.75.75 0 0 0 0 1.5h7.5a.75.75 0 0 0 0-1.5zM7 11.75a.75.75 0 0 1 .75-.75h6.5a.75.75 0 0 1 0 1.5h-6.5a.75.75 0 0 1-.75-.75M9.75 15a.75.75 0 0 0 0 1.5h6.5a.75.75 0 0 0 0-1.5z"/><path class="fill-white" d="M2 3.75C2 2.784 2.784 2 3.75 2h16.5c.966 0 1.75.784 1.75 1.75v16.5A1.75 1.75 0 0 1 20.25 22H3.75A1.75 1.75 0 0 1 2 20.25Zm1.75-.25a.25.25 0 0 0-.25.25v16.5c0 .138.112.25.25.25h16.5a.25.25 0 0 0 .25-.25V3.75a.25.25 0 0 0-.25-.25Z"/></svg>
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Kegiatan Ekstrakurikuler</h1>
                  <p class="text-base text-white">Berbagai kegiatan seperti hackathon, workshop, dan seminar untuk meningkatkan keterampilan dan wawasan siswa.</p>
                </div>
              </div>
            </div>
          </div>
        </div>  
      </section>

    </div>
  </main>
</template>
