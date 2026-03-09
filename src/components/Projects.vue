<script setup lang="ts">
import img1 from "../assets/projects/EnglishCourses.png";
import img2 from "../assets/projects/Login.png";
import img3 from "../assets/projects/LoveLifeHealth.png";
import img4 from "../assets/projects/Butik.png";
import img5 from "../assets/projects/Coffe.png";
import img6 from "../assets/projects/Surat.png";

import { ArrowTopRightOnSquareIcon } from "@heroicons/vue/24/outline";
import { CodeBracketIcon } from "@heroicons/vue/24/outline";

const projects = [
  {
    title: "English Courses",
    desc: "Website kursus bahasa Inggris.",
    image: img1,
    live: "https://sandyivanotumoka.github.io/LandingpageEnglishCR/",
    github: "https://github.com/sandyivanotumoka/LandingpageEnglishCR",
  },

  {
    title: "Login UI",
    desc: "UI login modern dengan desain split screen.",
    image: img2,
    live: "https://sandyivanotumoka.github.io/Login/",
    github: "https://github.com/sandyivanotumoka/Login",
  },

  {
    title: "LoveLife Health",
    desc: "Aplikasi diagnosis gejala penyakit.",
    image: img3,
    live: "https://sandyivanotumoka.github.io/lovelife-health/",
    github: "https://github.com/sandyivanotumoka/lovelife-health",
  },

  {
    title: "MyStoree Boutique",
    desc: "Website butik modern dengan landing page fashion.",
    image: img4,
    live: "https://sandyivanotumoka.github.io/Mystoree/",
    github: "https://github.com/sandyivanotumoka/Mystoree",
  },

  {
    title: "Coffee Shop",
    desc: "Website coffee shop dengan hero section modern.",
    image: img5,
    live: "https://sandyivanotumoka.github.io/coffe-shop/",
    github: "https://github.com/sandyivanotumoka/coffe-shop",
  },

  {
    title: "Agenda Persuratan",
    desc: "Sistem agenda persuratan dengan halaman login.",
    image: img6,
    live: "https://sandyivanotumoka.github.io/App-Surat/index.html",
    github: "https://github.com/sandyivanotumoka/App-Surat",
  },
];
</script>

<template>
  <section id="projects" class="py-28 px-6 md:px-10">
    <div class="max-w-6xl mx-auto">
      <!-- TITLE -->

      <div class="text-center mb-16">
        <p class="text-sm tracking-widest text-gray-500 mb-3">PROJECTS</p>

        <h2 class="text-3xl md:text-4xl font-bold">My Projects</h2>
      </div>

      <!-- PROJECT GRID -->

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-10">
        <div
          v-for="project in projects"
          :key="project.title"
          class="border border-black rounded-xl overflow-hidden hover:shadow-xl transition"
        >
          <!-- IMAGE -->

          <a :href="project.live" target="_blank">
            <img
              :src="project.image"
              class="w-full h-56 object-cover hover:scale-105 transition duration-300 cursor-pointer"
            />
          </a>

          <!-- CONTENT -->

          <div class="p-6">
            <h3 class="text-xl font-semibold mb-2">
              {{ project.title }}
            </h3>

            <p class="text-gray-600 mb-4">
              {{ project.desc }}
            </p>

            <!-- BUTTONS -->

            <div class="flex gap-4">
              <a
                :href="project.live"
                target="_blank"
                class="flex items-center gap-2 bg-black text-[#FFFDF2] px-4 py-2 rounded-lg hover:opacity-80 transition"
              >
                <ArrowTopRightOnSquareIcon class="w-5 h-5" />
                Live Demo
              </a>

              <a
                :href="project.github"
                target="_blank"
                class="flex items-center gap-2 border border-black px-4 py-2 rounded-lg hover:bg-black hover:text-[#FFFDF2] transition"
              >
                <CodeBracketIcon class="w-5 h-5" />
                GitHub
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
