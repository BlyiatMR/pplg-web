<script setup>
import NavbarVue from '@/components/Navbar.vue';
import HeroSection from '@/components/HomeComponent/HeroSection.vue'
import AboutSection from '@/components/HomeComponent/AboutSection.vue'
import WhyChoose from '@/components/HomeComponent/WhyChoose.vue';
import Testimonial from '@/components/HomeComponent/Testimonial.vue';
import Cta from '@/components/Cta.vue';
import Footer from '@/components/Footer.vue';

</script>
<script>
import gsap from "gsap";

export default {
  name: "Home",
  mounted() {
    this.animateIntro();
  },
  methods: {
    animateIntro() {
      const tl = gsap.timeline();
      tl.fromTo(
          "#imgs",
          { opacity: 0, x: 50 },
          { opacity: 1, x: 0, duration: 1 },
          "-=0.5"
        )
        .fromTo(
          this.$refs.content,
          { opacity: 0, y: 50 },
          { opacity: 1, y: 0, duration: 1 },
          "-=0.8"
        )
        .fromTo(
          "#title",
          { opacity: 0, x: -50 },
          { opacity: 1, x: 0, duration: 1 },
          "-=0.5"
        )
        .fromTo(
          "#description",
          { opacity: 0, x: 50 },
          { opacity: 1, x: 0, duration: 1 },
          "-=0.5"
        )
        .fromTo(
          "#btn",
          { opacity: 0, x: 50 },
          { opacity: 1, x: 0, duration: 1 },
          "-=0.5"
        );
    },
  },
};
</script>

<template>
  <main>

    <div class="relative overflow-hidden z-50">
      
      <div class="w-[65rem] h-[65rem] max-2xl:w-[55rem] bg-white rounded-full absolute -left-[30rem] opacity-10 -z-50"></div>
      <div class="w-[75rem] h-[75rem] bg-white rounded-full absolute -top-[5rem] -left-[30rem] opacity-10 -z-50"></div>

      <div class="w-[55rem] h-[55rem] border border-white rounded-full absolute top-20 -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[30rem] opacity-10 -z-50"></div>
      <div class="w-[75rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[30rem] opacity-10 -z-50"></div>

      <NavbarVue />

      <HeroSection />

      <AboutSection />

      <WhyChoose />

      <Testimonial />

      <Cta />

      <Footer />

    </div>
  </main>
</template>
