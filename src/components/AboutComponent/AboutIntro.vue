<template>
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
</template>

<script setup>
defineProps(['siswa', 'alumni', 'siswaScroll', 'alumniScroll'])
</script>