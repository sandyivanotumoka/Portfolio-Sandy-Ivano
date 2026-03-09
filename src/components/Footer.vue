<script setup lang="ts">
import { ArrowUp, Github, Linkedin, Instagram } from "lucide-vue-next";

function scrollTop() {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
}
</script>

<template>
  <footer
    class="relative mt-20 px-6 md:px-10 py-12 backdrop-blur-md bg-white/60 border-t border-gray-200"
  >
    <div class="max-w-6xl mx-auto">
      <div class="flex flex-col md:flex-row justify-between items-center gap-8">
        <!-- COPYRIGHT -->

        <p class="text-gray-500 text-sm">
          © 2026 Sandy Ivano. All rights reserved.
        </p>

        <!-- FOOTER NAVIGATION -->

        <div class="flex gap-6 text-sm">
          <a href="#home" class="hover:opacity-60 transition"> Home </a>

          <a href="#about" class="hover:opacity-60 transition"> About </a>

          <a href="#projects" class="hover:opacity-60 transition"> Projects </a>

          <a href="#contact" class="hover:opacity-60 transition"> Contact </a>
        </div>

        <!-- SOCIAL ICONS -->

        <div class="flex gap-5">
          <a
            href="https://github.com/sandyivanotumoka"
            target="_blank"
            class="hover:scale-110 transition"
          >
            <Github class="w-5 h-5" />
          </a>

          <a
            href="https://linkedin.com/in/username"
            target="_blank"
            class="hover:scale-110 transition"
          >
            <Linkedin class="w-5 h-5" />
          </a>

          <a
            href="https://instagram.com/sndyivn0"
            target="_blank"
            class="hover:scale-110 transition"
          >
            <Instagram class="w-5 h-5" />
          </a>
        </div>
      </div>
    </div>

    <!-- SCROLL TO TOP BUTTON -->

    <button
      @click="scrollTop"
      class="fixed bottom-6 right-6 bg-black text-white p-3 rounded-full shadow-lg hover:scale-110 transition"
    >
      <ArrowUp class="w-5 h-5" />
    </button>
  </footer>
</template>
