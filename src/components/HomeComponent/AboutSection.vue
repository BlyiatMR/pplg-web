<template>
    <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1280px] mx-auto">
        <!-- <div class="max-w-6xl flex items-center gap-40 mx-auto">
          <div>
            <img class="w-[20rem]" src="/src/assets/images/boy.png" alt="">
          </div>
          <div>
            <h1 class="font-semibold text-4xl text-slate-800">Selamat Datang di Jurusan PPLG</h1>
            <p class="max-w-5xl text-slate-600 text-base mt-5">Kami sangat bangga menyambut kalian di jurusan Pengembangan Perangkat Lunak dan Gim (PPLG), tempat kreativitas bertemu teknologi. Di sini, kalian akan belajar dan berkembang menjadi talenta muda yang siap menghadapi era digital. <br><br>Kami percaya, setiap langkah kecil yang kalian ambil di jurusan ini akan menjadi pijakan menuju mimpi besar. Jadi, mari manfaatkan setiap kesempatan untuk belajar, berinovasi, dan berkarya. <br><br>Selamat menikmati perjalanan belajar di PPLG! Jika ada tantangan, ingat, kalian tidak sendiri—kami ada untuk mendukung dan membimbing kalian. <br><br>Semangat berkarya, generasi hebat masa depan!</p>
          </div>
        </div> -->
          <div id="about" class="flex flex-wrap items-center justify-between">
            <div class="relative">
              <div class="w-fit bg-[#7743DB] rounded-3xl py-2 px-5 absolute top-5 right-0 flex items-center gap-5">
                <svg class="w-10" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 15 16"><path class="fill-white" d="M7.5 7a2.5 2.5 0 0 1 0-5a2.5 2.5 0 0 1 0 5m0-4C6.67 3 6 3.67 6 4.5S6.67 6 7.5 6S9 5.33 9 4.5S8.33 3 7.5 3"/><path class="fill-white" d="M13.5 11c-.28 0-.5-.22-.5-.5s.22-.5.5-.5s.5-.22.5-.5A2.5 2.5 0 0 0 11.5 7h-1c-.28 0-.5-.22-.5-.5s.22-.5.5-.5c.83 0 1.5-.67 1.5-1.5S11.33 3 10.5 3c-.28 0-.5-.22-.5-.5s.22-.5.5-.5A2.5 2.5 0 0 1 13 4.5c0 .62-.22 1.18-.6 1.62c1.49.4 2.6 1.76 2.6 3.38c0 .83-.67 1.5-1.5 1.5m-12 0C.67 11 0 10.33 0 9.5c0-1.62 1.1-2.98 2.6-3.38c-.37-.44-.6-1-.6-1.62A2.5 2.5 0 0 1 4.5 2c.28 0 .5.22.5.5s-.22.5-.5.5C3.67 3 3 3.67 3 4.5S3.67 6 4.5 6c.28 0 .5.22.5.5s-.22.5-.5.5h-1A2.5 2.5 0 0 0 1 9.5c0 .28.22.5.5.5s.5.22.5.5s-.22.5-.5.5m9 3h-6c-.83 0-1.5-.67-1.5-1.5v-1C3 9.57 4.57 8 6.5 8h2c1.93 0 3.5 1.57 3.5 3.5v1c0 .83-.67 1.5-1.5 1.5m-4-5A2.5 2.5 0 0 0 4 11.5v1c0 .28.22.5.5.5h6c.28 0 .5-.22.5-.5v-1A2.5 2.5 0 0 0 8.5 9z"/></svg> 
                <p class="text-base font-semibold text-white">200+ Alumni</p></div>
              <img class="object-cover object-top rounded-tl-2xl rounded-tr-[10rem] rounded-bl-[10rem] rounded-br-2xl w-[37rem] h-[20rem]" src="/src/assets/images/class.jpg" alt="">
              <div class="w-fit bg-[#7743DB] rounded-3xl py-2 px-5 absolute bottom-5 flex items-center gap-5">
                <svg class="w-10" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 15 16"><path class="fill-white" d="M7.5 7a2.5 2.5 0 0 1 0-5a2.5 2.5 0 0 1 0 5m0-4C6.67 3 6 3.67 6 4.5S6.67 6 7.5 6S9 5.33 9 4.5S8.33 3 7.5 3"/><path class="fill-white" d="M13.5 11c-.28 0-.5-.22-.5-.5s.22-.5.5-.5s.5-.22.5-.5A2.5 2.5 0 0 0 11.5 7h-1c-.28 0-.5-.22-.5-.5s.22-.5.5-.5c.83 0 1.5-.67 1.5-1.5S11.33 3 10.5 3c-.28 0-.5-.22-.5-.5s.22-.5.5-.5A2.5 2.5 0 0 1 13 4.5c0 .62-.22 1.18-.6 1.62c1.49.4 2.6 1.76 2.6 3.38c0 .83-.67 1.5-1.5 1.5m-12 0C.67 11 0 10.33 0 9.5c0-1.62 1.1-2.98 2.6-3.38c-.37-.44-.6-1-.6-1.62A2.5 2.5 0 0 1 4.5 2c.28 0 .5.22.5.5s-.22.5-.5.5C3.67 3 3 3.67 3 4.5S3.67 6 4.5 6c.28 0 .5.22.5.5s-.22.5-.5.5h-1A2.5 2.5 0 0 0 1 9.5c0 .28.22.5.5.5s.5.22.5.5s-.22.5-.5.5m9 3h-6c-.83 0-1.5-.67-1.5-1.5v-1C3 9.57 4.57 8 6.5 8h2c1.93 0 3.5 1.57 3.5 3.5v1c0 .83-.67 1.5-1.5 1.5m-4-5A2.5 2.5 0 0 0 4 11.5v1c0 .28.22.5.5.5h6c.28 0 .5-.22.5-.5v-1A2.5 2.5 0 0 0 8.5 9z"/></svg> 
                <p class="text-base font-semibold text-white">100+ Siswa</p></div>
            </div>
            <div class="max-w-xl space-y-5">
              <h1 class="max-w-7xl mx-auto font-semibold text-4xl text-slate-800 leading-tight">Tentang Jurusan PPLG</h1>
              <p class="text-base font-medium text-slate-600">Jurusan PPLG salah satu program keahlian SMK Negeri 1 Pangkep di bidang teknologi informasi yang berfokus pada pembelajaran tentang pembuatan, pengembangan, dan pengelolaan perangkat lunak (software) serta gim (game). <br><br> Jurusan ini bertujuan untuk mencetak lulusan yang kompeten dalam merancang aplikasi, membangun website, menciptakan gim interaktif, serta memahami prinsip-prinsip teknologi pemrograman modern.</p>
              <div class="flex pt-5 gap-10">
                <a id="btn" href="#about" class="flex w-[190px] justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-semibold hover:w-[200px] duration-300">Lebih Detail <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
              </div>
            </div>
          </div>
          <h1 class="max-w-7xl mx-auto text-center mt-20 font-semibold text-4xl text-slate-800 leading-tight">Program Keahlian</h1>
          <div class="relative max-w-7xl mx-auto flex gap-5 flex-wrap justify-around mt-10">

            <div class="group hover:bg-[#7743DB] hover:-translate-y-2 duration-300 py-5 px-6 rounded-3xl">
              <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="none" class="stroke-slate-800 group-hover:stroke-white duration-300" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" color="currentColor"><path d="M20 14.5v-8c0-1.886 0-2.828-.586-3.414S17.886 2.5 16 2.5H8c-1.886 0-2.828 0-3.414.586S4 4.614 4 6.5v8m-.502 1.015L4.02 14.5h15.932l.55 1.015c1.443 2.662 1.803 3.993 1.254 4.989s-2.002.996-4.91.996H7.154c-2.909 0-4.363 0-4.911-.996c-.549-.996-.19-2.327 1.254-4.989"/><path d="m15.5 7l.92.793c.387.333.58.5.58.707s-.193.374-.58.707L15.5 10m-7-3l-.92.793c-.387.333-.58.5-.58.707s.193.374.58.707L8.5 10M13 6l-2 5"/></g></svg>
              <div class="mt-5">
                <h1 class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">Web Development</h1>
                <p class="w-72 mt-2 text-base text-slate-600 group-hover:text-white duration-300">Membuat website interaktif dengan teknologi modern.</p>
              </div>
            </div>
            <div class="border-r max-xl:hidden"></div>
            <div class="group hover:bg-[#7743DB] hover:-translate-y-2 duration-300 py-5 px-6 rounded-3xl">
              <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16"><path class="fill-slate-800 group-hover:fill-white duration-300" d="M11.5 4a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1zM11 6.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 0 1h-2a.5.5 0 0 1-.5-.5m.5 1.5a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1z"/><path class="fill-slate-800 group-hover:fill-white duration-300" fill-rule="evenodd" d="M3 1C1.34 1 0 2.34 0 4v8c0 1.66 1.34 3 3 3h10c1.66 0 3-1.34 3-3V4c0-1.66-1.34-3-3-3zm10 1h-3v12h3c1.1 0 2-.895 2-2V4c0-1.1-.895-2-2-2M3 2h6v12H3c-1.1 0-2-.895-2-2V4c0-1.1.895-2 2-2" clip-rule="evenodd"/></svg>
              <div class="mt-5">
                <h1 class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">UI/UX</h1>
                <p class="w-72 mt-2 text-base text-slate-600 group-hover:text-white duration-300">Mendesain antarmuka menarik dan user-friendly.</p>
              </div>
            </div>
            <div class="border-r max-xl:hidden"></div>
            <div class="group hover:bg-[#7743DB] hover:-translate-y-2 duration-300 py-5 px-6 rounded-3xl">
              <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="none" class="stroke-slate-800 group-hover:stroke-white duration-300" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 8c.01-2.644.108-4.059 1.024-4.975C7.049 2 8.699 2 11.999 2s4.95 0 5.975 1.025c.916.916 1.013 2.33 1.023 4.975M5 16c.01 2.644.108 4.059 1.024 4.975C7.049 22 8.699 22 11.999 22s4.95 0 5.975-1.025c.916-.916 1.013-2.33 1.023-4.975M11 19h2m3-9l1.227 1.057c.515.445.773.667.773.943s-.258.498-.773.943L16 14m-8-4l-1.227 1.057C6.258 11.502 6 11.724 6 12s.258.498.773.943L8 14m5-5l-2 6" color="currentColor"/></svg>
              <div class="mt-5">
                <h1 class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">Mobile Development</h1>
                <p class="w-72 mt-2 text-base text-slate-600 group-hover:text-white duration-300">Membangun aplikasi Android sesuai standar industri.</p>
              </div>
            </div>
            <hr class="w-full max-lg:hidden">
            <div class="group hover:bg-[#7743DB] hover:-translate-y-2 duration-300 py-5 px-6 rounded-3xl">
              <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 36 36"><path class="fill-slate-800 group-hover:fill-white duration-300" d="M30.86 20.94a4.7 4.7 0 0 1 1.86.64h.05a15.1 15.1 0 0 0-.61-8.37a1 1 0 0 0-1.28-.59a1 1 0 0 0-.59 1.28a13.2 13.2 0 0 1 .57 7.04m-4.53 7.64a13 13 0 0 1-6.07 2.82a1 1 0 1 0 .17 2h.18a15.16 15.16 0 0 0 7.21-3.4v-.07a4.7 4.7 0 0 1-1.49-1.35m-10.71 2.76a13.2 13.2 0 0 1-4.29-1.61a15 15 0 0 1-1.63-1.11A4.7 4.7 0 0 1 8.24 30a16 16 0 0 0 2.07 1.48a15.4 15.4 0 0 0 4.94 1.86h.19a1 1 0 0 0 .18-2M4.56 21.15a4 4 0 0 0 .6-.09A13 13 0 0 1 5.7 14a1 1 0 0 0-1.88-.69a15 15 0 0 0-.56 8.43a4.8 4.8 0 0 1 1.3-.59"/><path class="fill-slate-800 group-hover:fill-white duration-300" d="M31.9 23a3.2 3.2 0 0 0-2.43-.42a3.3 3.3 0 0 0-1.4.77l-3.87-2.24a6.87 6.87 0 0 0-2.77-8.43l-.11-.07a6.6 6.6 0 0 0-2.42-.81V8a3.22 3.22 0 0 0 1.88-1.5A3.3 3.3 0 0 0 19.65 2a3.15 3.15 0 0 0-2.42-.32a3.24 3.24 0 0 0-2 1.51a3.3 3.3 0 0 0 1.13 4.46a3 3 0 0 0 .74.35v3.8a6.64 6.64 0 0 0-4.86 3.28a6.85 6.85 0 0 0-.42 6l-4 2.29a4 4 0 0 0-.45-.34A3.2 3.2 0 0 0 3 24.21a3.3 3.3 0 0 0 1.1 4.46a3.2 3.2 0 0 0 1.65.46a3 3 0 0 0 .78-.1a3.24 3.24 0 0 0 2.29-4.11l3.88-2.24a7.1 7.1 0 0 0 1.89 1.71a6.49 6.49 0 0 0 8.73-1.7l3.83 2.21a3.29 3.29 0 0 0 1.45 3.64a3.15 3.15 0 0 0 1.64.46A3.17 3.17 0 0 0 33 27.41A3.3 3.3 0 0 0 31.9 23M7 26.62a1.4 1.4 0 0 1-.91.64A1.36 1.36 0 0 1 5 27.11a1.48 1.48 0 0 1-.5-2a1.4 1.4 0 0 1 .88-.66a1.3 1.3 0 0 1 .34-.05a1.4 1.4 0 0 1 .75.22a1.48 1.48 0 0 1 .53 2m9.78-22.53a1.4 1.4 0 0 1 .88-.66a1.3 1.3 0 0 1 .34-.05a1.4 1.4 0 0 1 .72.2a1.48 1.48 0 0 1 .5 2a1.4 1.4 0 0 1-.88.66a1.36 1.36 0 0 1-1.06-.15a1.48 1.48 0 0 1-.5-2m2.41 19.32a4.8 4.8 0 0 1-3.68-.54A5.07 5.07 0 0 1 13.78 16A4.88 4.88 0 0 1 18 13.57a4.8 4.8 0 0 1 2.46.67a5.07 5.07 0 0 1 1.73 6.87a4.86 4.86 0 0 1-3 2.3m12.25 3.08a1.45 1.45 0 0 1-.88.67A1.36 1.36 0 0 1 29.5 27a1.48 1.48 0 0 1-.5-2a1.4 1.4 0 0 1 .9-.72a2 2 0 0 1 .34 0a1.3 1.3 0 0 1 .69.19a1.48 1.48 0 0 1 .51 2.02M8.05 10a13 13 0 0 1 5.35-3.77a5 5 0 0 1-.17-2.07a15.15 15.15 0 0 0-6.7 4.51A1 1 0 0 0 8.05 10"/><path class="fill-slate-800 group-hover:fill-white duration-300" d="M24.67 7.23A13.1 13.1 0 0 1 27.93 10a1 1 0 1 0 1.52-1.3a15 15 0 0 0-3.76-3.2a16 16 0 0 0-2.94-1.33a4.8 4.8 0 0 1-.15 2.06a14 14 0 0 1 2.07 1"/><path fill="none" d="M0 0h36v36H0z"/></svg>
              <div class="mt-5">
                <h1 class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">IoT</h1>
                <p class="w-72 mt-2 text-base text-slate-600 group-hover:text-white duration-300">Mengembangkan hardware dengan internet.</p>
              </div>
            </div>
            <div class="border-r max-xl:hidden"></div>
            <div class="group hover:bg-[#7743DB] hover:-translate-y-2 duration-300 py-5 px-6 rounded-3xl">
              <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path class="fill-slate-800 group-hover:fill-white duration-300" d="M4.5 3A1.5 1.5 0 0 0 3 4.5v2A1.5 1.5 0 0 0 4.5 8H5v3.84a1 1 0 0 0-.207.16L3 13.793a1 1 0 0 0 0 1.414L4.793 17a1 1 0 0 0 1.414 0L8 15.207q.094-.095.16-.207H12v.5a1.5 1.5 0 0 0 1.5 1.5h2a1.5 1.5 0 0 0 1.5-1.5v-2a1.5 1.5 0 0 0-1.5-1.5h-2a1.5 1.5 0 0 0-1.5 1.5v.5H8.16a1 1 0 0 0-.16-.207L6.207 12A1 1 0 0 0 6 11.84V8h.5A1.5 1.5 0 0 0 8 6.5v-2A1.5 1.5 0 0 0 6.5 3zM4 4.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5zm-.293 10L5.5 12.707L7.293 14.5L5.5 16.293zM13.5 13h2a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5v-2a.5.5 0 0 1 .5-.5"/></svg>
              <div class="mt-5">
                <h1 class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">Flowchart</h1>
                <p class="w-72 mt-2 text-base text-slate-600 group-hover:text-white duration-300">Representasi visual dari proses menggunakan simbol.</p>
              </div>
            </div>
            <div class="border-r max-xl:hidden"></div>
            <div class="group hover:bg-[#7743DB] hover:-translate-y-2 duration-300 py-5 px-6 rounded-3xl">
              <svg class="w-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path class="fill-slate-800 group-hover:fill-white duration-300" d="M7.25 7A.75.75 0 0 1 8 6.25h8a.75.75 0 0 1 0 1.5H8A.75.75 0 0 1 7.25 7M8 9.75a.75.75 0 0 0 0 1.5h5a.75.75 0 0 0 0-1.5z"/><path class="fill-slate-800 group-hover:fill-white duration-300" fill-rule="evenodd" d="M9.945 1.25c-1.367 0-2.47 0-3.337.117c-.9.12-1.658.38-2.26.981c-.602.602-.86 1.36-.981 2.26c-.117.867-.117 1.97-.117 3.337v8.11c0 1.367 0 2.47.117 3.337c.12.9.38 1.658.981 2.26c.602.602 1.36.86 2.26.982c.867.116 1.97.116 3.337.116h4.11c1.367 0 2.47 0 3.337-.116c.9-.122 1.658-.38 2.26-.982s.86-1.36.982-2.26c.116-.867.116-1.97.116-3.337v-8.11c0-1.367 0-2.47-.116-3.337c-.122-.9-.38-1.658-.982-2.26s-1.36-.86-2.26-.981c-.867-.117-1.97-.117-3.337-.117zM5.41 3.409c.277-.277.665-.457 1.4-.556c.754-.101 1.756-.103 3.191-.103h4c1.435 0 2.436.002 3.192.103c.734.099 1.122.28 1.399.556c.277.277.457.665.556 1.4c.101.754.103 1.756.103 3.191v7.25H7.782c-.818 0-1.376 0-1.855.128a3.8 3.8 0 0 0-1.177.548V8c0-1.435.002-2.437.103-3.192c.099-.734.28-1.122.556-1.399m-.632 14.84c.015.354.039.665.076.943c.099.734.28 1.122.556 1.399c.277.277.665.457 1.4.556c.754.101 1.756.103 3.191.103h4c1.435 0 2.436-.002 3.192-.103c.734-.099 1.122-.28 1.399-.556c.277-.277.457-.665.556-1.4c.083-.615.099-1.395.102-2.441H7.898c-.978 0-1.32.006-1.583.077a2.25 2.25 0 0 0-1.538 1.422" clip-rule="evenodd"/></svg>
              <div class="mt-5">
                <h1 class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">Belajar Umum</h1>
                <p class="w-72 mt-2 text-base text-slate-600 group-hover:text-white duration-300">Mencakup pembelajaran umum selain jurusan</p>
              </div>
            </div>
          </div>
        </div>
      </section>
</template>