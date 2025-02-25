<script setup>
import Navbar from '@/components/Navbar.vue';
import Cta from '@/components/Cta.vue';
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
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-24 py-20">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Profil Jurusan</h1>
            <div class="mx-auto text-center">
              <a class="text-base font-medium text-white text-center">Beranda > Profil</a>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-white py-20 space-y-20">
        <div class="flex flex-wrap justify-between items-center max-w-[1280px] mx-auto max-xl:mx-5">
         <div class="max-w-xl space-y-5">
          <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Jurusan Pengembangan Perangkat Lunak dan Gim</h1>
          <p class="text-base font-medium text-slate-600">Salah satu program keahlian SMK Negeri 1 Pangkajene dan Kepulauan di bidang teknologi informasi yang berfokus pada pembelajaran tentang pembuatan, pengembangan, dan pengelolaan perangkat lunak (software) serta gim (game). <br><br> Jurusan ini bertujuan untuk mencetak lulusan yang kompeten dalam merancang aplikasi, membangun website, menciptakan gim interaktif, serta memahami prinsip-prinsip teknologi pemrograman modern. <br><br>Melalui kurikulum yang terus diperbarui sesuai dengan perkembangan teknologi, jurusan ini menjadi pilihan yang tepat bagi siswa yang ingin menjadi bagian dari ekosistem digital yang dinamis dan inovatif.</p>
         </div>
         <div>
          <img src="/src/assets/images/pplg-logo.png" alt="">
         </div>
        </div>
        <div class="flex flex-wrap items-center justify-between max-w-[1280px] mx-auto max-xl:mx-5">
          <div>
            <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Menjalin Kerjasama</h1>
          </div>
          <div class="flex items-center justify-center gap-10">
            <div>
              <img src="/src/assets/images/ruparaya.png" class="w-40" alt="">
            </div>
            <div>
              <img src="/src/assets/images/metronix.png" class="w-40" alt="">
            </div>
            <div>
              <img src="/src/assets/images/yuscorp.png" class="w-40" alt="">
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20">
        <div class="flex flex-wrap justify-between items-center max-w-[1280px] mx-auto max-xl:mx-5">
          <div>
            <img src="/src/assets/images/class.jpg" class="object-cover object-top rounded-3xl w-[37rem] h-[38rem]" alt="">
          </div>
          <div class="max-w-xl">
            <div class="space-y-5">
              <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Visi</h1>
              <p class="text-base font-medium text-slate-600">Menjadi jurusan unggulan dalam bidang teknologi informasi yang mencetak lulusan inovatif, kreatif, dan kompeten dalam pengembangan perangkat lunak serta gim, berlandaskan profesionalisme dan nilai-nilai luhur.</p>
            </div>
            <div class="mt-10 space-y-5">
              <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Misi</h1>
              <p class="text-base font-medium text-slate-600">1. Membekali siswa dengan kemampuan pemrograman, desain, dan pengelolaan perangkat lunak serta gim berbasis teknologi terkini.</p>
              <p class="text-base font-medium text-slate-600">2. Menciptakan lingkungan pembelajaran yang mendukung pengembangan ide-ide kreatif dan inovatif di bidang teknologi informasi.</p>
              <p class="text-base font-medium text-slate-600">3. Menjalin kerja sama strategis dengan perusahaan teknologi untuk memberikan pengalaman praktik langsung melalui magang, pelatihan, dan sertifikasi.</p>
              <p class="text-base font-medium text-slate-600">4. Membentuk lulusan yang tidak hanya kompeten secara teknis, tetapi juga memiliki etika kerja, tanggung jawab, dan kemampuan beradaptasi dengan perkembangan teknologi global.</p>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-white py-20">
        <div class="max-w-[1280px] flex justify-between flex-wrap items-center mx-auto max-xl:mx-5">
          <div class="max-w-md relative">
            <h1 class="max-w-sm font-semibold sm:text-4xl text-3xl text-slate-800 tracking-wide leading-tight">Guru-Guru Inspiratif PPLG</h1>
            <p class="text-base font-medium text-slate-600 mt-5">Didukung oleh tim pengajar profesional yang berpengalaman di bidang teknologi informasi.</p>
            <div class="flex gap-5 mt-5">
              <a href="#" class="bg-yellow-400 p-4 rounded-full hover:-translate-y-1 duration-300">
                <svg class="w-7 h-7 rotate-180" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg>
              </a>
              <a href="#" class="bg-yellow-400 p-4 rounded-full hover:-translate-y-1 duration-300">
                <svg class="w-7 h-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg>
              </a>
            </div>      
          </div>
          <div class="flex flex-wrap gap-10 justify-center py-20">
            <div 
              v-for="(profile, index) in profiles" 
              :key="index" 
              class="w-[38rem] relative flex border-2 border-slate-200 rounded-3xl"
            >
              <img 
                :src="profile.img" 
                class="rounded-3xl w-60 h-96 object-cover" 
                alt=""
              />
              <div class="px-5 py-10">
                <p class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">
                  {{ profile.name }}
                </p>
                <p class="mt-2 text-base text-slate-600 duration-300">
                  {{ profile.position }}
                </p>
                <p class="mt-10 text-base text-slate-600 font-medium">
                  {{ profile.description }}
                </p>
                <div class="mt-10 flex flex-wrap gap-3">
                  <a href="" class="border border-slate-200 py-1 px-7 rounded-3xl">
                    <i class="fa-brands fa-instagram text-slate-600 text-2xl"></i>
                  </a>
                  <a href="" class="border border-slate-200 py-1 px-7 rounded-3xl">
                    <i class="fa-brands fa-facebook text-slate-600 text-2xl"></i>
                  </a>
                  <a href="" class="border border-slate-200 py-1 px-7 rounded-3xl">
                    <i class="fa-brands fa-x-twitter text-slate-600 text-2xl"></i>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <Cta />

      <Footer />
      </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      profiles: [
        {
          img: "/src/assets/images/teacher/pak_idris.jpeg",
          name: "Idris Suyupi",
          position: "Ketua Jurusan & Guru Produktif",
          description: "Membimbing siswa untuk memahami dan mengembangkan solusi berbasis IoT yang relevan dengan kebutuhan industri modern.",
        },
        // {
        //   img: "/src/assets/images/teacher/bu_ermi.jpeg",
        //   name: "Ermiwati",
        //   position: "Wali Kelas XII PPLG",
        //   description: "Membimbing siswa untuk memahami dan mengembangkan solusi berbasis IoT yang relevan dengan kebutuhan industri modern.",
        // },
        // {
        //   img: "/src/assets/images/teacher/bu_sul.jpeg",
        //   name: "Sulfitriani",
        //   position: "Wali Kelas XI PPLG",
        //   description: "Membimbing siswa untuk memahami dan mengembangkan solusi berbasis IoT yang relevan dengan kebutuhan industri modern.",
        // },
        // {
        //   img: "/src/assets/images/teacher/bu_sartika.jpeg",
        //   name: "Sartika",
        //   position: "Guru Produktif",
        //   description: "Membimbing siswa untuk memahami dan mengembangkan solusi berbasis IoT yang relevan dengan kebutuhan industri modern.",
        // },
        // {
        //   img: "/src/assets/images/teacher/bu_aisyah.jpeg",
        //   name: "Nur Aisyah Abdullah",
        //   position: "Guru Produktif",
        //   description: "Membimbing siswa untuk memahami dan mengembangkan solusi berbasis IoT yang relevan dengan kebutuhan industri modern.",
        // },
        // {
        //   img: "/src/assets/images/teacher/bu_indah.jpeg",
        //   name: "Indah Purnama Syahir",
        //   position: "Guru Produktif & Wali Kelas X PPLG",
        //   description: "Membimbing siswa untuk memahami dan mengembangkan solusi berbasis IoT yang relevan dengan kebutuhan industri modern.",
        // },
      ]
    };
  }
};
</script>