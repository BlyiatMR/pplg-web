<script setup>
import { ref, onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const typingText = ref(null)

onMounted(() => {
  const message = '. . .Tempat Para Developer Muda Berkembang dan Berkarya. . .'
  const letters = message.split('')

  typingText.value.innerHTML = ''

  letters.forEach((char) => {
    const span = document.createElement('span')
    span.textContent = char
    span.style.opacity = 0
    typingText.value.appendChild(span)
  })

  const spans = typingText.value.querySelectorAll('span')

  gsap.to(spans, {
    opacity: 1,
    duration: 0.05,
    stagger: 0.05,
    ease: 'power2.out',
    scrollTrigger: {
      trigger: typingText.value,
      start: 'top 80%', 
      toggleActions: 'play none none none',
    }
  })
})
</script>

<template>
    <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1280px] mx-auto max-xl:mx-5">
          <div id="about" class="">
            <div class="sm:space-y-16 space-y-6 ">
              <h1 ref="typingText" class="max-w-[1120px] mx-auto text-center font-medium sm:text-8xl text-3xl text-slate-800 tracking-wide"></h1>
              <div class="flex justify-center pt-5 gap-10">
                <a id="btn" href="/about" class="flex w-[190px] justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-semibold hover:w-[200px] duration-300">Lebih Detail <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
              </div>
            </div>
          </div>
          <div class="relative max-w-7xl mx-auto flex gap-5 flex-wrap justify-around mt-28">
            <div v-for="(item, index) in items" :key="index" class="relative overflow-hidden group hover:bg-[#7743DB] hover:-translate-y-2 duration-300 py-5 px-6 rounded-3xl">
              <svg class="w-20" xmlns="http://www.w3.org/2000/svg" :viewBox="item.viewBox" v-html="item.icon"></svg>
              <div class="mt-5 cursor-default">
                <h1 class="text-lg text-slate-800 group-hover:text-white duration-300 font-semibold">{{ item.title }}</h1>
                <p class="sm:w-72 w-fit mt-2 text-base text-slate-600 group-hover:text-white duration-300">{{ item.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: "Web Development",
          description: "Membuat website interaktif dengan teknologi modern.",
          viewBox: "0 0 24 24",
          icon: `<g fill="none" class="stroke-slate-800 group-hover:stroke-white duration-300" 
                  stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" color="currentColor">
                  <path d="M20 14.5v-8c0-1.886 0-2.828-.586-3.414S17.886 2.5 16 2.5H8c-1.886 0-2.828 0-3.414.586S4 4.614 4 6.5v8m-.502 1.015L4.02 14.5h15.932l.55 1.015c1.443 2.662 1.803 3.993 1.254 4.989s-2.002.996-4.91.996H7.154c-2.909 0-4.363 0-4.911-.996c-.549-.996-.19-2.327 1.254-4.989"/>
                  <path d="m15.5 7l.92.793c.387.333.58.5.58.707s-.193.374-.58.707L15.5 10m-7-3l-.92.793c-.387.333-.58.5-.58.707s.193.374.58.707L8.5 10M13 6l-2 5"/>
                </g>`
        },
        {
          title: "Game Development",
          description: "Membuat game interaktif dengan tools dan kreativitas.",
          viewBox: "0 0 24 24",
          icon: `<path fill="none" class="stroke-slate-800 group-hover:stroke-white duration-300" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M2 14.5c0-3.287 0-4.931.908-6.038a4 4 0 0 1 .554-.554C4.57 7 6.212 7 9.5 7h5c3.288 0 4.931 0 6.038.908a4 4 0 0 1 .554.554C22 9.57 22 11.212 22 14.5s0 4.931-.908 6.038a4 4 0 0 1-.554.554C19.43 22 17.788 22 14.5 22h-5c-3.287 0-4.931 0-6.038-.908a4 4 0 0 1-.554-.554C2 19.43 2 17.788 2 14.5M12 7V5a1 1 0 0 1 1-1a1 1 0 0 0 1-1V2m-4 14l-1.5-1.5m0 0L7 13m1.5 1.5L7 16m1.5-1.5L10 13m7 2.5v-2" color="currentColor"/>`
        },
        {
          title: "Mobile Development",
          description: "Membangun aplikasi Android sesuai standar industri.",
          viewBox: "0 0 24 24",
          icon: `<path fill="none" class="stroke-slate-800 group-hover:stroke-white duration-300" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 8c.01-2.644.108-4.059 1.024-4.975C7.049 2 8.699 2 11.999 2s4.95 0 5.975 1.025c.916.916 1.013 2.33 1.023 4.975M5 16c.01 2.644.108 4.059 1.024 4.975C7.049 22 8.699 22 11.999 22s4.95 0 5.975-1.025c.916-.916 1.013-2.33 1.023-4.975M11 19h2m3-9l1.227 1.057c.515.445.773.667.773.943s-.258.498-.773.943L16 14m-8-4l-1.227 1.057C6.258 11.502 6 11.724 6 12s.258.498.773.943L8 14m5-5l-2 6" color="currentColor"/>`
        },
        {
          title: "UI/UX Design",
          description: "Mendesain antarmuka menarik dan user-friendly.",
          viewBox: "0 0 16 16",
          icon: `<path class="fill-slate-800 group-hover:fill-white duration-300" d="M11.5 4a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1zM11 6.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 0 1h-2a.5.5 0 0 1-.5-.5m.5 1.5a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1z"/><path class="fill-slate-800 group-hover:fill-white duration-300" fill-rule="evenodd" d="M3 1C1.34 1 0 2.34 0 4v8c0 1.66 1.34 3 3 3h10c1.66 0 3-1.34 3-3V4c0-1.66-1.34-3-3-3zm10 1h-3v12h3c1.1 0 2-.895 2-2V4c0-1.1-.895-2-2-2M3 2h6v12H3c-1.1 0-2-.895-2-2V4c0-1.1.895-2 2-2" clip-rule="evenodd"/>`
        },
        {
          title: "IoT",
          description: "Mengembangkan hardware dengan internet.",
          viewBox: "0 0 36 36",
          icon: `<path class="fill-slate-800 group-hover:fill-white duration-300" d="M30.86 20.94a4.7 4.7 0 0 1 1.86.64h.05a15.1 15.1 0 0 0-.61-8.37a1 1 0 0 0-1.28-.59a1 1 0 0 0-.59 1.28a13.2 13.2 0 0 1 .57 7.04m-4.53 7.64a13 13 0 0 1-6.07 2.82a1 1 0 1 0 .17 2h.18a15.16 15.16 0 0 0 7.21-3.4v-.07a4.7 4.7 0 0 1-1.49-1.35m-10.71 2.76a13.2 13.2 0 0 1-4.29-1.61a15 15 0 0 1-1.63-1.11A4.7 4.7 0 0 1 8.24 30a16 16 0 0 0 2.07 1.48a15.4 15.4 0 0 0 4.94 1.86h.19a1 1 0 0 0 .18-2M4.56 21.15a4 4 0 0 0 .6-.09A13 13 0 0 1 5.7 14a1 1 0 0 0-1.88-.69a15 15 0 0 0-.56 8.43a4.8 4.8 0 0 1 1.3-.59"/><path class="fill-slate-800 group-hover:fill-white duration-300" d="M31.9 23a3.2 3.2 0 0 0-2.43-.42a3.3 3.3 0 0 0-1.4.77l-3.87-2.24a6.87 6.87 0 0 0-2.77-8.43l-.11-.07a6.6 6.6 0 0 0-2.42-.81V8a3.22 3.22 0 0 0 1.88-1.5A3.3 3.3 0 0 0 19.65 2a3.15 3.15 0 0 0-2.42-.32a3.24 3.24 0 0 0-2 1.51a3.3 3.3 0 0 0 1.13 4.46a3 3 0 0 0 .74.35v3.8a6.64 6.64 0 0 0-4.86 3.28a6.85 6.85 0 0 0-.42 6l-4 2.29a4 4 0 0 0-.45-.34A3.2 3.2 0 0 0 3 24.21a3.3 3.3 0 0 0 1.1 4.46a3.2 3.2 0 0 0 1.65.46a3 3 0 0 0 .78-.1a3.24 3.24 0 0 0 2.29-4.11l3.88-2.24a7.1 7.1 0 0 0 1.89 1.71a6.49 6.49 0 0 0 8.73-1.7l3.83 2.21a3.29 3.29 0 0 0 1.45 3.64a3.15 3.15 0 0 0 1.64.46A3.17 3.17 0 0 0 33 27.41A3.3 3.3 0 0 0 31.9 23M7 26.62a1.4 1.4 0 0 1-.91.64A1.36 1.36 0 0 1 5 27.11a1.48 1.48 0 0 1-.5-2a1.4 1.4 0 0 1 .88-.66a1.3 1.3 0 0 1 .34-.05a1.4 1.4 0 0 1 .75.22a1.48 1.48 0 0 1 .53 2m9.78-22.53a1.4 1.4 0 0 1 .88-.66a1.3 1.3 0 0 1 .34-.05a1.4 1.4 0 0 1 .72.2a1.48 1.48 0 0 1 .5 2a1.4 1.4 0 0 1-.88.66a1.36 1.36 0 0 1-1.06-.15a1.48 1.48 0 0 1-.5-2m2.41 19.32a4.8 4.8 0 0 1-3.68-.54A5.07 5.07 0 0 1 13.78 16A4.88 4.88 0 0 1 18 13.57a4.8 4.8 0 0 1 2.46.67a5.07 5.07 0 0 1 1.73 6.87a4.86 4.86 0 0 1-3 2.3m12.25 3.08a1.45 1.45 0 0 1-.88.67A1.36 1.36 0 0 1 29.5 27a1.48 1.48 0 0 1-.5-2a1.4 1.4 0 0 1 .9-.72a2 2 0 0 1 .34 0a1.3 1.3 0 0 1 .69.19a1.48 1.48 0 0 1 .51 2.02M8.05 10a13 13 0 0 1 5.35-3.77a5 5 0 0 1-.17-2.07a15.15 15.15 0 0 0-6.7 4.51A1 1 0 0 0 8.05 10"/><path class="fill-slate-800 group-hover:fill-white duration-300" d="M24.67 7.23A13.1 13.1 0 0 1 27.93 10a1 1 0 1 0 1.52-1.3a15 15 0 0 0-3.76-3.2a16 16 0 0 0-2.94-1.33a4.8 4.8 0 0 1-.15 2.06a14 14 0 0 1 2.07 1"/><path fill="none" d="M0 0h36v36H0z"/>`
        },
        {
          title: "Flowchart",
          description: "Representasi visual dari proses menggunakan simbol.",
          viewBox: "0 0 20 20",
          icon: `<path class="fill-slate-800 group-hover:fill-white duration-300" d="M4.5 3A1.5 1.5 0 0 0 3 4.5v2A1.5 1.5 0 0 0 4.5 8H5v3.84a1 1 0 0 0-.207.16L3 13.793a1 1 0 0 0 0 1.414L4.793 17a1 1 0 0 0 1.414 0L8 15.207q.094-.095.16-.207H12v.5a1.5 1.5 0 0 0 1.5 1.5h2a1.5 1.5 0 0 0 1.5-1.5v-2a1.5 1.5 0 0 0-1.5-1.5h-2a1.5 1.5 0 0 0-1.5 1.5v.5H8.16a1 1 0 0 0-.16-.207L6.207 12A1 1 0 0 0 6 11.84V8h.5A1.5 1.5 0 0 0 8 6.5v-2A1.5 1.5 0 0 0 6.5 3zM4 4.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5zm-.293 10L5.5 12.707L7.293 14.5L5.5 16.293zM13.5 13h2a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5v-2a.5.5 0 0 1 .5-.5"/>`
        },
        {
          title: "Basis Data",
          description: "Penyimpanan data terorganisir untuk kemudahan akses.",
          viewBox: "0 0 24 24",
          icon: `<g class="stroke-slate-800 group-hover:stroke-white duration-300" fill="none" stroke-width="1.5"><path stroke-linecap="round" d="M4 18V6m16 0v12"/><path d="M12 10c4.418 0 8-1.79 8-4s-3.582-4-8-4s-8 1.79-8 4s3.582 4 8 4Zm8 2c0 2.21-3.582 4-8 4s-8-1.79-8-4m16 6c0 2.21-3.582 4-8 4s-8-1.79-8-4"/></g>`
        },
      ]
    };
  }
};
</script>

<style>

</style>