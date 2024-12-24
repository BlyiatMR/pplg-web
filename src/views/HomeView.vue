<script setup>
import NavbarVue from '@/components/Navbar.vue';
import HeroSection from '@/components/HomeComponent/HeroSection.vue'
import AboutSection from '@/components/HomeComponent/AboutSection.vue'

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

      <section class="">
        <div class="max-w-[1280px] relative mx-auto py-20">

          <div class="w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[30rem] opacity-10 -z-50"></div>
          <div class="w-[85rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[30rem] opacity-10 -z-50"></div>
          <div class="w-[105rem] h-[85rem] border border-white rounded-full absolute -top-[10rem] -right-[30rem] opacity-10 -z-50"></div>
          <div class="w-[125rem] h-[85rem] border border-white rounded-full absolute -top-[10rem] -right-[30rem] opacity-10 -z-50"></div>

          <h1 class="max-w-7xl mx-auto text-center font-semibold text-4xl text-white leading-tight">Keunggulan Jurusan</h1>
          <div class="flex justify-center flex-wrap py-20 space-y-10">
            <div class="flex flex-wrap gap-x-40">
              <div class="max-w-lg flex gap-5 items-start py-5">
                <img class="w-12" src="/src/assets/images/icon/icon-curicullum.png" alt="">
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Kurikulum Up-to-date</h1>
                  <p class="text-base text-white">Kurikulum dirancang agar sejalan dengan perkembangan teknologi terkini, menjadikan siswa siap bersaing di pasar kerja.</p>
                </div>
              </div>
              <div class="max-w-lg flex gap-5 items-start py-5">
                <img class="w-12" src="/src/assets/images/icon/icon-computer.png" alt="">
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Fasilitas Komputer</h1>
                  <p class="text-base text-white">Menyediakan lab komputer yang dirancang mendukung pengalaman belajar sesuai dengan kebutuhan industri saat ini.</p>
                </div>
              </div>
            </div>
            <div class="flex flex-wrap gap-x-40">
              <div class="max-w-lg flex gap-5 items-start py-5">
                <img class="w-12" src="/src/assets/images/icon/icon-job.png" alt="">
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Peluang Karir Luas</h1>
                  <p class="text-base text-white">Membuka jalan untuk berbagai profesi seperti web developer, mobile developer, UI/UX designer, atau pengembang IoT.</p>
                </div>
              </div>
              <div class="max-w-lg flex gap-5 items-start py-5">
                <img class="w-12" src="/src/assets/images/icon/icon-people.png" alt="">
                <div class="space-y-3">
                  <h1 class="text-lg text-white font-semibold">Kegiatan Ekstrakurikuler</h1>
                  <p class="text-base text-white">Memiliki ekstrakurikuler Zone IT, yang berfokus pada pembuatan website, mulai dari desain hingga pemrograman.</p>
                </div>
              </div>
            </div>
          </div>
        </div>  
      </section>

      <!-- <section class="h-screen bg-slate-50">
        <div class="max-w-[1280px] mx-auto py-20">
          <h1 class="font-semibold text-center text-4xl text-slate-800 tracking-wide leading-tight">Aktivitas Siswa PPLG</h1>
          <div class="space-y-5">
            <p class="max-w-xl text-3xl font-medium tracking-wide leading-tight">Jurusan PPLG bukan cuma belajar, banyak momen seperti ikut lomba dan study tour ke perusahaan IT. Itu semua menginspirasi saya untuk terus berkembang."</p>
            <div class="flex items-center gap-5">
              <img class="w-14 rounded-full" src="/src/assets/images/alumni.jpg" alt="">
              <div>
                <h1 class="text-lg font-semibold">Emil Kusmayadi</h1>
                <p>Alumni 2023</p>
              </div>
            </div>
          </div>
        </div>
      </section> -->

      <section class="bg-slate-50">
        <div class="max-w-[1280px] flex space-x-40 mx-auto py-20">
          <div class="max-w-xl relative">
            <h1 class="max-w-sm font-semibold text-4xl text-slate-800 tracking-wide leading-tight">Kata Alumni PPLG</h1>
            <p class="text-base font-medium text-slate-600 mt-5">Alumni kami telah membuktikan bahwa dengan semangat belajar dan ilmu yang didapat, mereka bisa meraih karier impian di bidang IT.</p>          
          </div>
          <div class="space-y-5">
            <p class="max-w-2xl text-2xl font-medium tracking-wide leading-tight">"Jurusan PPLG bukan cuma belajar, banyak momen seperti ikut lomba dan study tour ke perusahaan IT. Itu semua menginspirasi saya untuk terus berkembang."</p>
            <div class="flex items-center gap-5">
              <img class="w-16 rounded-full" src="/src/assets/images/alumni.jpg" alt="">
              <div>
                <h1 class="text-lg font-semibold">Emil Kusmayadi</h1>
                <p>Alumni 2023</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 pb-20">
        <div class="max-w-[1280px] relative overflow-hidden mx-auto pt-32">
          <div class="w-[40rem] h-[40rem] bg-white absolute -right-80 top-5 rounded-full opacity-10"></div>
          <div class="w-[50rem] h-[40rem] bg-white absolute -right-80 top-5 rounded-full opacity-10"></div>
          <img class="absolute right-10 top-0 w-[20rem]" src="/src/assets/images/boy-second.png" alt="">
          <div class="py-20 px-16 bg-[#7743DB] rounded-3xl">
            <h1 class="max-w-xl font-semibold text-4xl text-white tracking-wide leading-tight">Siap Menjadi Bagian dari Generasi Ahli Teknologi?</h1>
            <p class="max-w-xl text-base text-white mt-5">Bergabunglah bersama kami dan wujudkan impianmu menjadi ahli pemrograman, pengembang perangkat lunak, dan pencipta gim inovatif</p>
            <div class="flex pt-10 gap-10">
            <a id="btn" href="#about" class="flex w-[220px] justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-semibold hover:w-[230px] duration-300">Daftar Sekarang <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg></a>
          </div>
          </div>
        </div>
      </section>

      <footer class="">
        <div class="max-w-[1280px] relative mx-auto pt-20 pb-5">
          <div class="w-[65rem] h-[65rem] border border-white rounded-full absolute -right-[30rem] opacity-10 -z-50"></div>
          <div class="w-[85rem] h-[75rem] border border-white rounded-full absolute -top-[5rem] -right-[30rem] opacity-10 -z-50"></div>
          <div class="w-[105rem] h-[85rem] border border-white rounded-full absolute -top-[10rem] -right-[30rem] opacity-10 -z-50"></div>
          <div class="w-[125rem] h-[85rem] border border-white rounded-full absolute -top-[10rem] -right-[30rem] opacity-10 -z-50"></div>
          <div class="flex justify-between">
            <div class="max-w-md">
              <img class="w-20" src="/src/assets/images/pplg-logo.png" alt="">
              <p class="max-w-xs text-base text-white mt-5">Jurusan PPLG SMK Negeri 1 Pangkep berkomitmen mencetak generasi muda yang kompeten di bidang teknologi.</p>
              <div class="flex gap-5 mt-3">
                <a href="https://www.instagram.com/pplgsmkn1pangkep/"><i class="fa-brands fa-instagram text-2xl text-white opacity-70 hover:opacity-100 duration-300"></i></a>
                <a href="https://www.youtube.com/@pplg_smkn1pangkep/videos"><i class="fa-brands fa-youtube text-2xl text-white opacity-70 hover:opacity-100 duration-300"></i></a>
                <a href="#"><i class="fa-brands fa-facebook text-2xl text-white opacity-70 hover:opacity-100 duration-300"></i></a>
              </div>
              <div class="flex flex-col gap-5 mt-10">
                <div class="flex gap-3">
                  <i class="fa-solid fa-location-dot text-2xl text-white"></i>
                  <p class="max-w-xs text-base text-white">Jl. Sambung Jawa, Kec. Bungoro, Kabupaten Pangkep</p>
                </div>
                <div class="flex items-center gap-3">
                  <i class="fa-solid fa-envelope text-2xl text-white"></i>
                  <p class="max-w-xs text-base text-white">pplgsmknpangkep@gmail.com</p>
                </div>
              </div>
            </div>
            <div class="flex gap-20">
              <div class="">
                <p class="max-w-xs text-base text-white mt-5 mb-5 font-semibold">Menu</p>
                <div class="flex flex-col gap-y-2 text-white">
                  <a href="#" class="opacity-70 hover:opacity-100 duration-300">Beranda</a>
                  <a href="#" class="opacity-70 hover:opacity-100 duration-300">Profil</a>
                  <a href="#" class="opacity-70 hover:opacity-100 duration-300">Alumni</a>
                  <a href="#" class="opacity-70 hover:opacity-100 duration-300">Galeri</a>
                  <a href="#" class="opacity-70 hover:opacity-100 duration-300">Kontak</a>
                </div>
              </div>
              <div class="">
                <p class="max-w-xs text-base text-white mt-5 mb-5 font-semibold">Menu Sekolah</p>
                <div class="flex flex-col gap-y-2 text-white">
                  <a href="https://smkn1pangkep.sch.id/" target="_blank" class="opacity-70 hover:opacity-100 duration-300">Beranda</a>
                  <a href="https://smkn1pangkep.sch.id/halaman/visi-misi" target="_blank" class="opacity-70 hover:opacity-100 duration-300">Profil</a>
                  <a href="https://smkn1pangkep.sch.id/kalender-pendidikan" target="_blank" class="opacity-70 hover:opacity-100 duration-300">Kurikulum</a>
                  <a href="https://smkn1pangkep.sch.id/berita" target="_blank" class="opacity-70 hover:opacity-100 duration-300">Article News</a>
                  <a href="https://smkn1pangkep.sch.id/halaman/perpustakaan-lagaligo-smkn-1-pangkep" target="_blank" class="opacity-70 hover:opacity-100 duration-300">Perpustakaan</a>
                  <a href="https://smkn1pangkep.sch.id/produk" target="_blank" class="opacity-70 hover:opacity-100 duration-300">Toko Online</a>
                  <a href="https://smkn1pangkep.sch.id/alumni" target="_blank" class="opacity-70 hover:opacity-100 duration-300">Alumni</a>
                </div>
              </div>
            </div>
            <div>
              <div class="mapswrapper"><iframe class="rounded-3xl" width="450" height="300" loading="lazy" allowfullscreen src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBFw0Qbyq9zTFTd-tUY6dZWTgaQzuU17R8&q=Jl.%20Sambung%20Jawa%2C%20RT.002%2FRW.002%2C%20Samalewa%2C%20Kec.%20Pangkajene%2C%20Kabupaten%20Pangkajene%20Dan%20Kepulauan%2C%20Sulawesi%20Selatan%2090617&zoom=15&maptype=roadmap"></iframe><a href="https://taxinstructions.net/form-2106/"></a></div>
            </div>
          </div>
          <hr class="w-full opacity-20 mt-5">
          <div>
            <p class="text-base text-center text-white mt-5">© 2024 Jurusan PPLG SMKN 1 Pangkep. Seluruh Hak Cipta Dilindungi.</p>
          </div>
        </div>
      </footer>

    </div>
  </main>
</template>
