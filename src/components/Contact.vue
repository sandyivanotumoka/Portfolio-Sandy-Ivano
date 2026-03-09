<script setup lang="ts">
import {
  Mail,
  Github,
  Linkedin,
  Phone,
  Briefcase,
  Facebook,
  Instagram,
} from "lucide-vue-next";
</script>

<template>
  <section id="contact" class="py-28 px-6 md:px-10">
    <div class="max-w-4xl mx-auto text-center">
      <p class="text-sm tracking-widest text-gray-500 mb-3">CONTACT</p>

      <h2 class="text-3xl md:text-4xl font-bold mb-6">Get In Touch</h2>

      <p class="text-gray-600 mb-10">
        Jika tertarik bekerja sama atau ingin berdiskusi, silakan hubungi saya.
      </p>

      <div class="flex justify-center gap-6 flex-wrap">
        <!-- EMAIL -->

        <a
          href="mailto:emailkamu@gmail.com"
          class="flex items-center gap-2 border border-black px-6 py-3 rounded-lg hover:bg-black hover:text-white transition"
        >
          <Mail class="w-5 h-5" />
          Email
        </a>

        <!-- GITHUB -->

        <a
          href="https://github.com/username"
          target="_blank"
          class="flex items-center gap-2 border border-black px-6 py-3 rounded-lg hover:bg-black hover:text-white transition"
        >
          <Github class="w-5 h-5" />
          GitHub
        </a>

        <!-- LINKEDIN -->

        <a
          href="https://linkedin.com/in/username"
          target="_blank"
          class="flex items-center gap-2 border border-black px-6 py-3 rounded-lg hover:bg-black hover:text-white transition"
        >
          <Linkedin class="w-5 h-5" />
          LinkedIn
        </a>

        <!-- WHATSAPP -->

        <a
          href="https://wa.me/6282271551354"
          target="_blank"
          class="flex items-center gap-2 border border-black px-6 py-3 rounded-lg hover:bg-black hover:text-white transition"
        >
          <Phone class="w-5 h-5" />
          WhatsApp
        </a>

        <!-- JOBSTREET -->

        <a
          href="https://id.jobstreet.com/id/profile/me"
          target="_blank"
          class="flex items-center gap-2 border border-black px-6 py-3 rounded-lg hover:bg-black hover:text-white transition"
        >
          <Briefcase class="w-5 h-5" />
          JobStreet
        </a>

        <!-- FACEBOOK -->

        <a
          href="https://facebook.com/sandy.tumoka.9"
          target="_blank"
          class="flex items-center gap-2 border border-black px-6 py-3 rounded-lg hover:bg-black hover:text-white transition"
        >
          <Facebook class="w-5 h-5" />
          Facebook
        </a>

        <!-- INSTAGRAM -->

        <a
          href="https://instagram.com/sndyivn0"
          target="_blank"
          class="flex items-center gap-2 border border-black px-6 py-3 rounded-lg hover:bg-black hover:text-white transition"
        >
          <Instagram class="w-5 h-5" />
          Instagram
        </a>
      </div>
    </div>
  </section>
</template>
