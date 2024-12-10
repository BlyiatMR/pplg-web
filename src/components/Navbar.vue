<script>
    export default {
    data() {
        return {
        isMenuOpen: false,
        isDarkMode: true
        };
    },
    methods: {
        toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen;
        },
        toggleDarkMode() {
          this.isDarkMode = !this.isDarkMode;
          if (this.isDarkMode) {
            document.documentElement.classList.add('dark');
          } else {
            document.documentElement.classList.remove('dark');
          }
        }
    }
    };
</script>
<template>
    <nav class="max-w-[1440px] mx-28 pt-5">
      <div class="hidden lg:flex text-white justify-between items-center flex">
        <a href="#" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Beranda</a>
        <a href="#" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Profil</a>
        <a href="#" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Alumni</a>
        <img class="w-16" src="/src/assets/images/pplg-logo.png" alt="">
        <a href="#" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Kerja Sama</a>
        <a href="#" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Galeri</a>
        <a href="#" class="hover:bg-white hover:bg-opacity-10 py-2 px-3 duration-300 rounded-xl">Kontak</a>
      </div>

      <!-- Mobile Menu Icon -->
      <div class="lg:hidden flex justify-between">
        <img class="w-16" src="/src/assets/images/pplg-logo.png" alt="">
          <button class="text-white" @click="toggleMenu">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" stroke="currentColor" class="w-8 h-8">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
      </div>

      <div v-if="isMenuOpen" class="lg:hidden bg-white bg-opacity-80 backdrop-blur-md shadow-2xl shadow-slate-950 border-t border-gray-700">
        <div class="flex flex-col items-center gap-4 py-5 text-gray-400">
          <a href="#" class="font-semibold tracking-wide hover:text-gray-300 duration-300">Beranda</a>
          <a href="#" class="font-semibold tracking-wide hover:text-gray-300 duration-300">Profil Jurusan</a>
          <a href="#" class="font-semibold tracking-wide hover:text-gray-300 duration-300">Alumni</a>
          <a href="#" class="font-semibold tracking-wide hover:text-gray-300 duration-300">Kerja Sama</a>
          <a href="#" class="font-semibold tracking-wide hover:text-gray-300 duration-300">Galeri</a>
          <a href="#" class="font-semibold tracking-wide hover:text-gray-300 duration-300">Kontak</a>
        </div>
      </div>
    </nav>
</template>