<script setup>
import { ref } from 'vue'
import BgCircles from '@/components/BgCircles.vue';
import Navbar from '@/components/Navbar.vue';
import Cta from '@/components/Cta.vue';
import Footer from '@/components/Footer.vue';

const name = ref('')
const email = ref('')
const subject = ref('')
const message = ref('')
const success = ref(false)

function sendToWhatsApp() {
  const phone = '62895338056836' // Nomor WhatsApp tujuan tanpa +
  let pesan = 'Halo, saya ingin menghubungi PPLG SMKN 1 Pangkep.%0A%0A'
  if (name.value) pesan += `Nama: ${name.value}%0A`
  if (email.value) pesan += `Email: ${email.value}%0A`
  if (subject.value) pesan += `Pertanyaan: ${subject.value}%0A`
  if (message.value) pesan += `Pesan: ${message.value}%0A`
  const url = `https://wa.me/${phone}?text=${pesan}`
  window.open(url, '_blank')
  // Reset form dan tampilkan notifikasi sukses
  success.value = true
  name.value = ''
  email.value = ''
  subject.value = ''
  message.value = ''
  setTimeout(() => { success.value = false }, 4000)
}
</script>

<template>
  <main>
    <div class="relative overflow-hidden z-50">
      <BgCircles />
      <Navbar />

      <section class="z-50">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5">
          <div class="max-w-4xl mx-auto w-fit space-y-5 sm:pt-52 pb-20 pt-40">
            <h1 id="title" class="sm:text-4xl text-3xl text-white font-semibold tracking-wide text-center leading-tight">Kontak Jurusan</h1>
            <div class="mx-auto text-center">
              <p class="text-base font-medium text-white"><a href="/" class="mr-3">Beranda</a> <span class="mr-3 text-gray-300">/</span> Kontak</p>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-slate-50 py-20 space-y-20">
        <div class="max-w-[1240px] mx-auto max-xl:mx-5 flex flex-wrap justify-around items-center gap-10">
          <div class="max-w-xl space-y-7">
            <h1 class="sm:text-4xl text-3xl font-semibold tracking-wide leading-tight">Hubungi Kami</h1>
            <div class="space-y-1">
              <p class="text-lg text-slate-800 font-semibold">Alamat</p>
              <p class="sm:text-lg text-base font-medium text-slate-600">SMK Negeri 1 Pangkajene dan Kepulauan <br>Jl. Sambung Jawa, Kec. Bungoro, Kabupaten Pangkep</p>
            </div>
            <div class="space-y-1">
              <p class="text-lg text-slate-800 font-semibold">Telepon</p>
              <p class="sm:text-lg text-base font-medium text-slate-600">+62 853-4225-5394 <br>Senin – Jumat, 08.00 – 16.00 WITA</p>
            </div>
            <div class="space-y-1">
              <p class="text-lg text-slate-800 font-semibold">Email</p>
              <p class="sm:text-lg text-base font-medium text-slate-600">pplgsmknpangkep@gmail.com</p>
            </div>
            <div class="space-y-1">
              <p class="text-lg text-slate-800 font-semibold">Media Sosial</p>
              <div class="space-x-5">
                <a href="https://www.instagram.com/pplgsmkn1pangkep/"><i class="fa-brands fa-instagram text-2xl text-slate-800 opacity-70 hover:opacity-100 duration-300"></i></a>
                <a href="https://www.youtube.com/@pplg_smkn1pangkep/videos"><i class="fa-brands fa-youtube text-2xl text-slate-800 opacity-70 hover:opacity-100 duration-300"></i></a>
                <a href="#"><i class="fa-brands fa-facebook text-2xl text-slate-800 opacity-70 hover:opacity-100 duration-300"></i></a>
              </div>
            </div>
          </div>
          <div class="max-w-xl border border-slate-200 shadow-xl py-10 sm:px-16 px-8 rounded-3xl">
            <p class="sm:text-lg text-base font-medium text-slate-600 text-center">
              Gunakan informasi kontak berikut atau isi formulir untuk mengirimkan pesan/pertanyaan kepada kami seputar jurusan PPLG
            </p>
            <div class="mt-4 mb-6 bg-yellow-100 border-l-4 border-yellow-400 text-yellow-800 p-4 rounded text-sm">
              <span class="font-bold">*</span> Kolom bertanda bintang wajib diisi.<br>
              Pastikan data yang Anda masukkan sudah benar sebelum mengirimkan pesan.
            </div>
            <form @submit.prevent="sendToWhatsApp" class="mt-5">
              <div v-if="success" class="mb-4 bg-green-100 border-l-4 border-green-500 text-green-700 p-4 rounded text-sm">
                Pesan berhasil dikirim! Silakan lanjutkan pengiriman di WhatsApp.
              </div>
              <div class="grid sm:grid-cols-2 grid-cols-1 sm:gap-5 gap-2">
                <div>
                  <input v-model="name" type="text" placeholder="Nama Lengkap*" required class="text-gray-700/80 block w-full py-2 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg">
                </div>
                <div>
                  <input v-model="email" type="email" placeholder="Email" class="text-gray-700/80 block w-full py-2 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg">
                </div>
              </div>
              <div class="mt-4">
                <input v-model="subject" type="text" placeholder="Subjek Pertanyaan*" required class="text-gray-700/80 block w-full py-2 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg">
              </div>
              <div>
                <textarea v-model="message" placeholder="Deskripsi" class="text-gray-700/80 block w-full py-5 px-4 mt-2 bg-white border border-gray-300 focus:ring-transparent focus:border-gray-700/25 rounded-lg h-32"></textarea>
              </div>
              <div class="mt-10 flex justify-center">
                <button type="submit" class="flex w-fit justify-between bg-yellow-400 py-2 px-5 rounded-lg tracking-wide font-semibold hover:w-[128px] duration-300">
                  Kirim
                  <svg class="w-7" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 9"><path fill="currentColor" d="M12.5 5h-9c-.28 0-.5-.22-.5-.5s.22-.5.5-.5h9c.28 0 .5.22.5.5s-.22.5-.5.5"/><path fill="currentColor" d="M10 8.5a.47.47 0 0 1-.35-.15c-.2-.2-.2-.51 0-.71l3.15-3.15l-3.15-3.15c-.2-.2-.2-.51 0-.71s.51-.2.71 0l3.5 3.5c.2.2.2.51 0 .71l-3.5 3.5c-.1.1-.23.15-.35.15Z"/></svg>
                </button>
              </div>
            </form>
          </div>
        </div>
      </section>

      <Cta />
      <Footer />
    </div>
  </main>
</template>