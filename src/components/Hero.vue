<script setup lang="ts">
import { onMounted } from "vue";
import profile from "../assets/profile.jpeg";
import gsap from "gsap";

onMounted(() => {
  gsap.from(".hero-title", {
    y: 50,
    opacity: 0,
    duration: 1,
  });

  gsap.from(".hero-text", {
    y: 30,
    opacity: 0,
    duration: 1,
    delay: 0.5,
  });

  gsap.from(".hero-btn", {
    opacity: 0,
    duration: 1,
    delay: 1,
  });

  gsap.from(".hero-img", {
    x: -80,
    opacity: 0,
    duration: 1,
  });
});
</script>

<template>
  <section
    id="home"
    class="pt-32 md:pt-40 min-h-screen flex items-center px-6 md:px-10 relative overflow-hidden"
  >
    <!-- Animasi -->
    <div
      class="absolute w-96 h-96 bg-black/5 rounded-full top-10 left-10 animate-float-slow"
    ></div>

    <div
      class="absolute w-80 h-80 bg-black/10 rounded-full bottom-10 right-10 animate-float-slow delay-1000"
    ></div>
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-16 items-center">
      <!-- FOTO -->
      <div class="flex justify-center hero-img">
        <img
          :src="profile"
          class="w-64 h-64 rounded-full object-cover border-4 border-black"
        />
      </div>

      <!-- TEXT -->
      <div class="text-center md:text-left">
        <p class="text-gray-600 dark:text-gray-400 mb-3 hero-text">
          Halo, Nama saya
        </p>

        <h1 class="text-4xl md:text-6xl font-bold mb-6 hero-title">
          Sandy Ivano
        </h1>

        <p class="text-lg text-gray-700 dark:text-white mb-8 hero-text">
          Saya seorang Frontend Developer yang fokus membuat website modern
          menggunakan Vue dan React.
        </p>

        <div
          class="flex justify-center md:justify-start gap-5 flex-wrap hero-btn"
        >
          <button
            class="bg-black text-[#FFFDF2] px-7 py-3 rounded-lg hover:scale-105 hover:opacity-90 transition"
          >
            Lihat Project
          </button>

          <button
            class="border border-black px-7 py-3 rounded-lg hover:bg-black hover:text-white transition"
          >
            Contact
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
