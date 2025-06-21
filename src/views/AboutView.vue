<script setup>
import { ref, onMounted, onUnmounted, nextTick } from 'vue'
import BgCircles from '@/components/BgCircles.vue';
import Navbar from '@/components/Navbar.vue';
import Cta from '@/components/Cta.vue';
import Footer from '@/components/Footer.vue';
import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
import InnerPageHero from '@/components/InnerPageHero.vue'
import AboutIntro from '@/components/AboutComponent/AboutIntro.vue'
import AboutVisiMisi from '@/components/AboutComponent/AboutVisiMisi.vue'
import AboutGuruCarousel from '@/components/AboutComponent/AboutGuruCarousel.vue'

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

const carouselRef = ref(null)
let tl = null

onMounted(async () => {
  await nextTick()
  const cards = carouselRef.value.querySelectorAll('.carousel-card')
  const cardWidth = cards[0].offsetWidth + 40 // 40px gap-10
  const originalCards = profiles.length
  const loopWidth = cardWidth * originalCards

  tl = gsap.timeline({ repeat: -1, defaults: { ease: "none" } })
  tl.to(carouselRef.value, {
    x: `-=${loopWidth}`,
    duration: originalCards * 5,
    modifiers: {
      x: gsap.utils.unitize(x => parseFloat(x) % loopWidth)
    }
  })
})

onUnmounted(() => {
  if (tl) tl.kill()
})
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">

      <BgCircles />

      <Navbar />

      <InnerPageHero title="Profil Jurusan" breadcrumb="Profil" />

      <AboutIntro :siswa="siswa" :alumni="alumni" :siswaScroll="siswaScroll" :alumniScroll="alumniScroll" />

      <AboutVisiMisi />

      <AboutGuruCarousel :profiles="profiles" :profilesh="profilesh" />

      <Cta />

      <Footer />
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      profilesh: [
        {
          img: new URL('@/assets/images/teacher/pak_idris.jpeg', import.meta.url).href,
          name: "Drs. Syahruddin Rahmat",
          position: "Kepala UPT SMKN 1 Pangkep",
        },
        {
          img: new URL('@/assets/images/teacher/pak_idris.jpeg', import.meta.url).href,
          name: "Idris Suyupi",
          position: "Ketua Jurusan PPLG",
        },
      ],
      profiles: [
        {
          img: new URL('@/assets/images/teacher/pak_idris.jpeg', import.meta.url).href,
          name: "Idris Suyupi",
          position: "Guru Produktif",
        },
        {
          img: new URL('@/assets/images/teacher/bu_aisyah.jpeg', import.meta.url).href,
          name: "Nur Aisyah Abdullah",
          position: "Guru Produktif",
        },
        {
          img: new URL('@/assets/images/teacher/bu_sartika.jpeg', import.meta.url).href,
          name: "Sartika",
          position: "Guru Produktif",
        },
        {
          img: new URL('@/assets/images/teacher/bu_indah.jpeg', import.meta.url).href,
          name: "Indah Purnama Syahir",
          position: "Guru Produktif",
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