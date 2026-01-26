<script setup>
import Stars from "~/components/Stars.vue";
import Services from "~/components/Services.vue";
</script>

<template>
  <div class="relative pt-32 pb-20 px-6 min-h-screen bg-[#020408]">
    <Stars />

    <!-- Hero Section -->
    <section class="relative z-10 max-w-4xl mx-auto text-center mb-20">
      <h1 class="text-5xl md:text-6xl font-extrabold mb-8 tracking-tight">
        Engineering with <span class="text-purple-400">Precision</span>
      </h1>
      <p class="text-xl text-gray-300 leading-relaxed max-w-3xl mx-auto">
        Discover our suite of high-performance digital solutions. We build
        robust, scalable, and forward-thinking software designed for security
        and massive scale.
      </p>
    </section>

    <!-- Content Components -->
    <Services />
  </div>
</template>
