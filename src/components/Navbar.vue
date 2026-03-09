<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";

const menuOpen = ref(false);
const scrolled = ref(false);
const darkMode = ref(false);

function handleScroll() {
  scrolled.value = window.scrollY > 40;
}

function toggleDark() {
  darkMode.value = !darkMode.value;
  document.documentElement.classList.toggle("dark");
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <nav
    :class="[
      'fixed top-0 left-0 w-full flex justify-between items-center px-8 py-5 z-50 transition-all duration-300',
      scrolled
        ? 'backdrop-blur-md bg-black/70 dark:bg-black/80 shadow-lg md:w-[90%] md:left-1/2 md:-translate-x-1/2 md:top-5 md:rounded-xl'
        : 'bg-white text-black dark:bg-black dark:text-white',
    ]"
  >
    <!-- LOGO -->

    <h1 class="text-xl font-bold">Portfolio</h1>

    <!-- DESKTOP MENU -->

    <ul class="hidden md:flex gap-8 items-center">
      <li>
        <a href="#home" class="hover:opacity-70">Home</a>
      </li>

      <li>
        <a href="#about" class="hover:opacity-70">About</a>
      </li>

      <li>
        <a href="#projects" class="hover:opacity-70">Projects</a>
      </li>

      <li>
        <a href="#contact" class="hover:opacity-70">Contact</a>
      </li>

      <!-- DARK MODE BUTTON -->
      <button
        @click="toggleDark"
        class="ml-4 w-14 h-7 flex items-center bg-gray-300 dark:bg-gray-600 rounded-full p-1 transition"
      >
        <div
          :class="[
            'w-5 h-5 bg-white rounded-full shadow-md transform transition',
            darkMode ? 'translate-x-7' : '',
          ]"
        ></div>
      </button>
    </ul>

    <!-- MOBILE BUTTON -->

    <button class="md:hidden text-2xl" @click="menuOpen = !menuOpen">☰</button>

    <!-- MOBILE MENU -->

    <div
      v-if="menuOpen"
      class="absolute top-full left-0 w-full bg-black text-[#FFFDF2] flex flex-col items-center gap-6 py-6 md:hidden z-50"
    >
      <a href="#home" @click="menuOpen = false">Home</a>
      <a href="#about" @click="menuOpen = false">About</a>
      <a href="#projects" @click="menuOpen = false">Projects</a>
      <a href="#contact" @click="menuOpen = false">Contact</a>

      <!-- DARK MODE MOBILE -->
      <button
        @click="toggleDark"
        class="ml-4 w-14 h-7 flex items-center bg-gray-300 dark:bg-gray-600 rounded-full p-1 transition"
      >
        <div
          :class="[
            'w-5 h-5 bg-white rounded-full shadow-md transform transition',
            darkMode ? 'translate-x-7' : '',
          ]"
        ></div>
      </button>
    </div>
  </nav>
</template>
