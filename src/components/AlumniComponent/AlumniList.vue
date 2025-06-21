<script setup>
const alumniYears = [2021, 2022, 2023, 2024, 2025]
</script>

<template>
  <section class="bg-slate-50 py-20 space-y-20">
    <div class="max-w-[1240px] mx-auto max-xl:mx-5">
      <div class="flex flex-wrap sm:gap-10 gap-5 justify-center">
        <div
          v-for="year in alumniYears"
          :key="year"
          class="max-w-fit flex gap-3 bg-yellow-400 rounded-3xl p-12 shadow-2xl hover:-translate-y-2 duration-300 cursor-pointer">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="text-slate-800" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="m19 5l-7-3l-7 3l3.5 1.5v2S9.667 8 12 8s3.5.5 3.5.5v-2zm0 0v4m-3.5-.5v1a3.5 3.5 0 1 1-7 0v-1m-.717 8.203c-1.1.685-3.986 2.082-2.229 3.831C6.413 21.39 7.37 22 8.571 22h6.858c1.202 0 2.158-.611 3.017-1.466c1.757-1.749-1.128-3.146-2.229-3.83a7.99 7.99 0 0 0-8.434 0" color="currentColor"/></svg>
          <h3 class="text-lg font-semibold text-slate-800">
            Alumni {{ year }}
          </h3>
        </div>
      </div>
    </div>
  </section>
</template>