<script setup>
import { ref, onMounted } from 'vue';
import BgCircles from '@/components/BgCircles.vue';
import Navbar from '@/components/Navbar.vue';
import Cta from '@/components/Cta.vue';
import Footer from '@/components/Footer.vue';
import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

const siswa = ref(0);
const alumni = ref(0);
const siswaScroll = ref(0);
const alumniScroll = ref(0);

onMounted(() => {
  gsap.registerPlugin(ScrollTrigger);

  // Count tanpa scroll
  gsap.to(siswa, {
    value: 250,
    duration: 3,
    onUpdate: () => {
      siswa.value = Math.floor(siswa.value);
    }
  });
  gsap.to(alumni, {
    value: 250,
    duration: 3,
    onUpdate: () => {
      alumni.value = Math.floor(alumni.value);
    }
  });

  // Count discroll
  gsap.to(siswaScroll, {
    value: 250,
    duration: 3,
    scrollTrigger: {
      trigger: "#count-section",
      start: "top 80%",
      once: true,
    },
    onUpdate: () => {
      siswaScroll.value = Math.floor(siswaScroll.value);
    }
  });
  gsap.to(alumniScroll, {
    value: 250,
    duration: 3,
    scrollTrigger: {
      trigger: "#count-section",
      start: "top 80%",
      once: true,
    },
    onUpdate: () => {
      alumniScroll.value = Math.floor(alumniScroll.value);
    }
  });
});
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">

      <BgCircles />

      <Navbar />

      <!-- Hero Section -->
      <section class="z-50">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
          <div class="max-w-fit mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">
              Profil Jurusan
            </h1>
            <div class="mx-auto text-center">
              <p class="text-base font-medium text-white"><a href="/" class="mr-3">Beranda</a> <span class="mr-3 text-gray-300">/</span> Profil</p>
            </div>
          </div>
        </div>
      </section>

      <!-- About Section -->
      <section class="bg-slate-50 py-20 space-y-10">
        <div class="flex flex-wrap justify-around gap-10 items-center max-w-[1240px] mx-auto max-xl:mx-5">
          <div class="max-w-xl space-y-5">
            <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">
              Mengenal Jurusan PPLG
            </h1>
            <p class="sm:text-lg text-base font-medium text-slate-600">
              <span class="font-semibold text-slate-800">Salah satu program keahlian SMK Negeri 1 Pangkajene dan Kepulauan</span> di bidang teknologi informasi yang berfokus pada pembelajaran tentang <span class="font-semibold text-slate-800">pembuatan, pengembangan, dan pengelolaan perangkat lunak (software) serta gim (game).</span>
              <br><br>
              Jurusan ini bertujuan untuk mencetak lulusan yang kompeten dalam <span class="font-semibold text-slate-800">merancang aplikasi, membangun website, menciptakan gim interaktif,</span> serta memahami prinsip-prinsip teknologi pemrograman modern.
              <br><br>
              Melalui <span class="font-semibold text-slate-800">kurikulum yang terus diperbarui</span> sesuai dengan perkembangan teknologi, jurusan ini menjadi pilihan yang tepat bagi siswa yang ingin menjadi bagian dari <span class="font-semibold text-slate-800">ekosistem digital yang dinamis dan inovatif.</span>
            </p>
          </div>
          <div id="count-section" class="relative max-sm:mt-10">
            <div class="max-sm:hidden absolute top-0 left-0 bg-primary px-5 py-[32px] rounded-3xl border-t-4 border-t-[#B79FEB] w-[149px] text-base text-center text-white font-medium leading-snug">
              <span class="text-xl font-semibold">{{ siswa }}+</span> <br>Total Siswa
            </div>
            <div class="max-sm:hidden absolute top-[115px] left-0 bg-primary px-5 py-[32px] border-t-4 border-t-[#B79FEB] rounded-3xl w-[149px] mt-[4px] text-base text-center text-white font-medium leading-snug">
              <span class="text-xl font-semibold">{{ alumni }}+</span> <br>Total Alumni
            </div>
            <img src="/src/assets/images/img-profile.png" class="w-[470px]" alt="">
          </div>
        </div>
        <div id="count-section" class="max-w-[1240px] mx-auto max-xl:mx-5">
          <div class="sm:hidden flex flex-wrap justify-center gap-4">
            <div class="w-[150px] bg-[#7743DB] border-t-4 border-t-[#B79FEB] rounded-3xl px-10 py-10 shadow-xl flex flex-col items-center gap-3">
              <p class="text-white font-semibold sm:text-4xl text-2xl tracking-wide">
                {{ siswaScroll }}+
              </p>
              <p class="text-white font-medium tracking-wide">Siswa</p>
            </div>
            <div class="w-[150px] bg-[#7743DB] border-t-4 border-t-[#B79FEB] rounded-3xl px-10 py-10 shadow-xl flex flex-col items-center gap-3">
              <p class="text-white font-semibold sm:text-4xl text-2xl tracking-wide">
                {{ alumniScroll }}+
              </p>
              <p class="text-white font-medium tracking-wide">Alumni</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Visi Misi Section -->
      <section class="bg-white py-20">
        <div class="flex flex-wrap justify-around items-center max-w-[1240px] mx-auto max-xl:mx-5">
          <div>
            <img src="/src/assets/images/class.jpg" class="object-cover object-top rounded-3xl w-[30rem] h-[25rem]" alt="">
          </div>
          <div class="max-w-xl">
            <div class="space-y-5 max-sm:mt-10">
              <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Visi</h1>
              <p class="sm:text-lg text-base font-medium text-slate-600">
                Menjadi jurusan unggulan dalam bidang teknologi informasi yang mencetak lulusan inovatif, kreatif, dan kompeten dalam pengembangan perangkat lunak serta gim, berlandaskan profesionalisme dan nilai-nilai luhur.
              </p>
            </div>
            <div class="mt-10 space-y-5">
              <h1 class="max-w-7xl mx-auto font-semibold sm:text-4xl text-3xl text-slate-800 leading-tight">Misi</h1>
              <p class="sm:text-lg text-base font-medium text-slate-600">
                1. Membekali siswa dengan kemampuan pemrograman, desain, dan pengelolaan perangkat lunak serta gim berbasis teknologi terkini.
              </p>
              <p class="sm:text-lg text-base font-medium text-slate-600">
                2. Menciptakan lingkungan pembelajaran yang mendukung pengembangan ide-ide kreatif dan inovatif di bidang teknologi informasi.
              </p>
              <p class="sm:text-lg text-base font-medium text-slate-600">
                3. Menjalin kerja sama strategis dengan perusahaan teknologi untuk memberikan pengalaman praktik langsung melalui magang, pelatihan, dan sertifikasi.
              </p>
              <p class="sm:text-lg text-base font-medium text-slate-600">
                4. Membentuk lulusan yang tidak hanya kompeten secara teknis, tetapi juga memiliki etika kerja, tanggung jawab, dan kemampuan beradaptasi dengan perkembangan teknologi global.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Guru Section -->
      <section class="bg-slate-50 py-20">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
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

<script>
export default {
  data() {
    return {
      profiles: [
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
      ]
    }
  }
}
</script>