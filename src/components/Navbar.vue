<script>
import { gsap } from "gsap";
import Swal from "sweetalert2";
import "sweetalert2/dist/sweetalert2.min.css";

export default {
  data() {
    return {
      isMenuOpen: false,
      isDarkMode: true,
      hasAnimatedNavbar: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
      const menu = this.$refs.mobileMenu;
      const overlay = this.$refs.menuOverlay;

      if (this.isMenuOpen) {
        document.body.classList.add("overflow-hidden");
        gsap.set(overlay, { display: "block", opacity: 0 });
        gsap.to(overlay, { opacity: 1, duration: 0.3 });
        gsap.set(menu, { display: "block" });
        gsap.fromTo(menu, { opacity: 0 }, { opacity: 1, duration: 0.5, ease: "power1.out" });
      } else {
        gsap.to(menu, {
          opacity: 0,
          duration: 0.4,
          ease: "power2.in",
          onComplete: () => {
            menu.style.display = "none";
            document.body.classList.remove("overflow-hidden");
          }
        });
        gsap.to(overlay, {
          opacity: 0,
          duration: 0.3,
          onComplete: () => {
            overlay.style.display = "none";
          }
        });
      }
    },
    handleScroll() {
      const navbar = this.$refs.navbar;
      if (!this.hasAnimatedNavbar && window.scrollY > 10) {
        this.hasAnimatedNavbar = true;
        gsap.fromTo(
          navbar,
          { y: "-100%", opacity: 0 },
          { y: "0%", opacity: 1, duration: 0.5, ease: "power2.out" }
        );
        navbar.classList.add("scrolled");
      }
      if (window.scrollY > 10) {
        navbar.classList.add("scrolled");
      } else {
        navbar.classList.remove("scrolled");
      }
    },
    toggleDarkMode() {
      this.isDarkMode = !this.isDarkMode;
      document.documentElement.classList.toggle("dark", this.isDarkMode);
    },
    showAktivitasPopup() {
      Swal.fire({
        title: 'Aktivitas Jurusan',
        html: `
          <div style="display:flex;flex-direction:column;align-items:center;justify-content:center;padding: 0 0 24px 0;">
            <svg width="90" height="90" viewBox="0 0 24 24" fill="none">
              <circle cx="12" cy="12" r="10" fill="#facc15"/>
              <path d="M8 12h8M12 8v8" stroke="#222" stroke-width="2" stroke-linecap="round"/>
            </svg>
            <div style="margin-top:18px;font-size:1.1rem;color:#fff;">Video aktivitas akan hadir di sini.</div>
          </div>
        `,
        width: 400,
        background: '#222',
        showCloseButton: true,
        showConfirmButton: false,
        customClass: {
          popup: 'rounded-2xl shadow-lg'
        }
      });
    }
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style scoped>
.scrolled {
  background-color: #7743DB !important;
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  transition: background-color 0.3s ease;
}
</style>

<template>
  <div>
    <!-- Navbar -->
    <nav ref="navbar" class="fixed top-0 left-0 w-full z-[999] bg-transparent transition-all duration-300 border-b border-white border-opacity-10 pb-5">
      <div class="max-w-[1100px] mx-auto pt-5 max-xl:mx-5">
        <!-- Desktop -->
        <div class="hidden lg:flex text-white justify-between items-center">
          <img class="w-14" src="/src/assets/images/pplg-logo.png" alt="">
          <div class="flex items-center gap-8 font-medium">
            <a href="/" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Beranda</a>
            <a href="/about" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Profil</a>
            <a href="/alumni" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Alumni</a>
            <a href="/organization" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Ekstrakurikuler</a>
            <a href="/gallery" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Galeri</a>
            <a href="/contact" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Kontak</a>
          </div>
          <button
            @click="showAktivitasPopup"
            class="w-fit flex items-center text-slate-800 gap-3 bg-yellow-400 py-1 px-4 rounded-lg tracking-wide font-semibold"
            style="outline:none;border:none;cursor:pointer"
          >
            <svg class="w-9 bg-yellow-400 p-2 rounded-full" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
              <path class="fill-black" d="M21.409 9.353a2.998 2.998 0 0 1 0 5.294L8.597 21.614C6.534 22.737 4 21.277 4 18.968V5.033c0-2.31 2.534-3.769 4.597-2.648z"/>
            </svg>
            Aktivitas
          </button>
        </div>
        <!-- Mobile -->
        <div class="lg:hidden flex justify-between items-center">
          <a href="/">
            <img class="w-12" src="/src/assets/images/pplg.png" alt="">
          </a>
          <button class="text-white" @click="toggleMenu">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </div>
    </nav>

    <!-- Overlay -->
    <div ref="menuOverlay"
         class="fixed inset-0 z-[9998] bg-black bg-opacity-40 backdrop-blur-sm hidden lg:hidden"
         @click="toggleMenu"></div>

    <!-- Mobile Menu -->
    <div
      ref="mobileMenu"
      class="fixed top-0 left-0 w-full h-screen z-[9999] bg-[#7743DB] text-white overflow-y-auto px-6 py-10 transition-transform duration-500 ease-in-out"
      style="display: none">
      <div class="flex justify-end pb-4">
        <button @click="toggleMenu" aria-label="Close Menu">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      <nav class="flex flex-col items-start gap-4 px-5">
        <a href="/" class="font-semibold tracking-wide hover:text-gray-200 duration-300">Beranda</a>
        <a href="/about" class="font-semibold tracking-wide hover:text-gray-200 duration-300">Profil</a>
        <a href="/alumni" class="font-semibold tracking-wide hover:text-gray-200 duration-300">Alumni</a>
        <a href="/organization" class="font-semibold tracking-wide hover:text-gray-200 duration-300">Ekstrakurikuler</a>
        <a href="/gallery" class="font-semibold tracking-wide hover:text-gray-200 duration-300">Galeri</a>
        <a href="/contact" class="font-semibold tracking-wide hover:text-gray-200 duration-300">Kontak</a>
        <div class="mt-5">
          <button
            @click="showAktivitasPopup"
            class="w-fit flex items-center text-slate-800 gap-3 bg-yellow-400 py-1 px-4 rounded-lg tracking-wide font-semibold"
            style="outline:none;border:none;cursor:pointer"
          >
            <svg class="w-9 bg-yellow-400 p-2 rounded-full" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
              <path class="fill-black" d="M21.409 9.353a2.998 2.998 0 0 1 0 5.294L8.597 21.614C6.534 22.737 4 21.277 4 18.968V5.033c0-2.31 2.534-3.769 4.597-2.648z"/>
            </svg>
            Aktivitas
          </button>
        </div>
        <footer class="mt-16">
          <div>
            <p class="text-xs text-white">pplgsmknpangkep@gmail.com</p>
            <div class="flex gap-5 mt-3">
              <a href="https://www.instagram.com/pplgsmkn1pangkep/"><i class="fa-brands fa-instagram text-2xl text-white opacity-70 hover:opacity-100 duration-300"></i></a>
              <a href="https://web.facebook.com/smkn1pangkep"><i class="fa-brands fa-facebook text-2xl text-white opacity-70 hover:opacity-100 duration-300"></i></a>
              <a href="https://www.youtube.com/@pplg_smkn1pangkep/videos"><i class="fa-brands fa-youtube text-2xl text-white opacity-70 hover:opacity-100 duration-300"></i></a>
            </div>
          </div>
        </footer>
      </nav>
    </div>
  </div>
</template>