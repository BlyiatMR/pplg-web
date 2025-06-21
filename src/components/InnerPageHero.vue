<template>
  <section class="z-50">
    <div class="max-w-[1240px] mx-auto max-xl:mx-5">
      <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
        <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">
          {{ title }}
        </h1>
        <div class="mx-auto text-center">
          <p class="text-base font-medium text-white">
            <a href="/" class="mr-3">Beranda</a>
            <span class="mr-3 text-gray-300">/</span> {{ breadcrumb }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  title: String,
  breadcrumb: String
})
</script>