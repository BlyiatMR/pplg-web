<script setup>
import NavbarVue from '@/components/Navbar.vue';
import HeroSection from '@/components/HomeComponent/HeroSection.vue'
import AboutSection from '@/components/HomeComponent/AboutSection.vue'
import WhyChoose from '@/components/HomeComponent/WhyChoose.vue';
import Testimonial from '@/components/HomeComponent/Testimonial.vue';
import Faq from '@/components/Faq.vue';
import Cta from '@/components/Cta.vue';
import Footer from '@/components/Footer.vue';
import BgCircles from '@/components/BgCircles.vue';
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
        );
    },
  },
};
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">
      <BgCircles />

      <NavbarVue />

      <HeroSection />

      <AboutSection />

      <WhyChoose />

      <Testimonial />

      <Faq />

      <Cta />

      <Footer />
    </div>
  </main>
</template>
