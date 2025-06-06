<script setup>
import { ref, onMounted } from 'vue';
import Navbar from '@/components/Navbar.vue';
import Cta from '@/components/Cta.vue';
import Footer from '@/components/Footer.vue';
import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

const siswa = ref(0);
const alumni = ref(0);

const profiles = ref([
  {
    img: new URL('@/assets/images/teacher/pak_idris.jpeg', import.meta.url).href,
    name: "Idris Suyupi",
    position: "Ketua Jurusan & Guru Produktif",
  },
  {
    img: new URL('@/assets/images/teacher/bu_sartika.jpeg', import.meta.url).href,
    name: "Sartika",
    position: "Guru Produktif",
  },
  {
    img: new URL('@/assets/images/teacher/bu_aisyah.jpeg', import.meta.url).href,
    name: "Nur Aisyah Abdullah",
    position: "Guru Produktif",
  },
  {
    img: new URL('@/assets/images/teacher/bu_indah.jpeg', import.meta.url).href,
    name: "Indah Purnama Syahir",
    position: "Guru Produktif & Wali Kelas X PPLG",
  },
  {
    img: new URL('@/assets/images/teacher/bu_sul.jpeg', import.meta.url).href,
    name: "Sulfitriani",
    position: "Wali Kelas XI PPLG",
  },
  {
    img: new URL('@/assets/images/teacher/bu_ermi.jpeg', import.meta.url).href,
    name: "Ermiwati Sahwa",
    position: "Wali Kelas XII PPLG",
  },
]);

onMounted(() => {
  gsap.registerPlugin(ScrollTrigger);

  gsap.to(siswa, {
    value: 250,
    duration: 2,
    scrollTrigger: {
      trigger: "#count-section",
      start: "top 80%",
      once: true,
    },
    onUpdate: () => {
      siswa.value = Math.floor(siswa.value);
    }
  });

  gsap.to(alumni, {
    value: 250,
    duration: 2,
    scrollTrigger: {
      trigger: "#count-section",
      start: "top 80%",
      once: true,
    },
    onUpdate: () => {
      alumni.value = Math.floor(alumni.value);
    }
  });
});
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">
      <!-- Background circles -->
      <div class="w-[65rem] h-[65rem] max-2xl:w-[55rem] bg-white rounded-full absolute -left-[30rem] opacity-10 -z-50"></div>
      <div class="w-[75rem] h-[75rem] bg-white rounded-full absolute -top-[5rem] -left-[30rem] opacity-10 -z-50"></div>
      <div class="w-[55rem] h-[55rem] border border-white rounded-full absolute top-20 -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[75rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[30rem] opacity-10 -z-50"></div>

      <Navbar />

      <!-- Hero Section -->
      <section class="z-50">
        <div class="max-w-[1100px] mx-auto max-xl:mx-5">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">
              Profil Jurusan
            </h1>
            <div class="mx-auto text-center">
              <a class="text-base font-medium text-white text-center">Beranda &gt; Profil</a>
            </div>
          </div>
        </div>
      </section>

      <!-- About Section -->
      <section class="bg-slate-50 py-20 space-y-20">
        <div class="flex flex-wrap justify-between items-center max-w-[1100px] mx-auto max-xl:mx-5">
          <div class="max-w-xl space-y-5">
            <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">
              Mengenal Jurusan PPLG
            </h1>
            <p class="text-base font-medium text-slate-600">
              Salah satu program keahlian SMK Negeri 1 Pangkajene dan Kepulauan di bidang teknologi informasi yang berfokus pada pembelajaran tentang pembuatan, pengembangan, dan pengelolaan perangkat lunak (software) serta gim (game).
              <br><br>
              Jurusan ini bertujuan untuk mencetak lulusan yang kompeten dalam merancang aplikasi, membangun website, menciptakan gim interaktif, serta memahami prinsip-prinsip teknologi pemrograman modern.
              <br><br>
              Melalui kurikulum yang terus diperbarui sesuai dengan perkembangan teknologi, jurusan ini menjadi pilihan yang tepat bagi siswa yang ingin menjadi bagian dari ekosistem digital yang dinamis dan inovatif.
            </p>
          </div>
          <div class="max-sm:mt-10">
            <img src="/src/assets/images/pplg.png" class="w-[400px]" alt="">
          </div>
        </div>
        <div id="count-section" class="max-w-[1100px] mx-auto max-xl:mx-5">
          <div class="max-w-full bg-[#7743DB] flex flex-wrap sm:justify-around justify-center max-sm:gap-10 rounded-3xl px-10 py-10 shadow-xl">
            <div class="flex flex-col items-center gap-3">
              <p class="text-white font-semibold sm:text-4xl text-3xl tracking-wide">
                {{ siswa }}+
              </p>
              <p class="text-white font-medium tracking-wide">Total Siswa</p>
            </div>
            <div class="flex flex-col items-center gap-3">
              <p class="text-white font-semibold sm:text-4xl text-3xl tracking-wide">
                {{ alumni }}+
              </p>
              <p class="text-white font-medium tracking-wide">Total Alumni</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Visi Misi Section -->
      <section class="bg-white py-20">
        <div class="flex flex-wrap justify-between items-center max-w-[1100px] mx-auto max-xl:mx-5">
          <div>
            <img src="/src/assets/images/class.jpg" class="object-cover object-top rounded-3xl w-[30rem] h-[25rem]" alt="">
          </div>
          <div class="max-w-xl">
            <div class="space-y-5 max-sm:mt-10">
              <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Visi</h1>
              <p class="text-base font-medium text-slate-600">
                Menjadi jurusan unggulan dalam bidang teknologi informasi yang mencetak lulusan inovatif, kreatif, dan kompeten dalam pengembangan perangkat lunak serta gim, berlandaskan profesionalisme dan nilai-nilai luhur.
              </p>
            </div>
            <div class="mt-10 space-y-5">
              <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Misi</h1>
              <p class="text-base font-medium text-slate-600">
                1. Membekali siswa dengan kemampuan pemrograman, desain, dan pengelolaan perangkat lunak serta gim berbasis teknologi terkini.
              </p>
              <p class="text-base font-medium text-slate-600">
                2. Menciptakan lingkungan pembelajaran yang mendukung pengembangan ide-ide kreatif dan inovatif di bidang teknologi informasi.
              </p>
              <p class="text-base font-medium text-slate-600">
                3. Menjalin kerja sama strategis dengan perusahaan teknologi untuk memberikan pengalaman praktik langsung melalui magang, pelatihan, dan sertifikasi.
              </p>
              <p class="text-base font-medium text-slate-600">
                4. Membentuk lulusan yang tidak hanya kompeten secara teknis, tetapi juga memiliki etika kerja, tanggung jawab, dan kemampuan beradaptasi dengan perkembangan teknologi global.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Guru Section -->
      <section class="bg-slate-50 py-20">
        <div class="max-w-[1100px] mx-auto max-xl:mx-5">
          <div class="relative">
            <h1 class="text-center font-semibold sm:text-4xl text-3xl text-slate-800 tracking-wide leading-tight">
              Guru-Guru Produktif PPLG
            </h1>
          </div>
          <div class="flex flex-wrap gap-10 mt-20 justify-center">
            <div
              v-for="(profile, index) in profiles"
              :key="index"
              class="relative bg-white rounded-3xl shadow-xl"
            >
              <img :src="profile.img" class="rounded-t-3xl w-80 h-96 object-cover" alt="" />
              <div class="justify-between items-end py-3 px-5">
                <div class="space-y-2">
                  <p class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">
                    {{ profile.name }}
                  </p>
                </div>
                <div class="flex items-center justify-between">
                  <div>
                    <p class="w-40 text-base text-slate-600 duration-300">
                      {{ profile.position }}
                    </p>
                  </div>
                  <div class="flex gap-3">
                    <a href="">
                      <i class="fa-brands fa-instagram text-slate-600 text-2xl"></i>
                    </a>
                    <a href="">
                      <i class="fa-brands fa-facebook text-slate-600 text-2xl"></i>
                    </a>
                    <a href="">
                      <i class="fa-brands fa-linkedin text-slate-600 text-2xl"></i>
                    </a>
                  </div>
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