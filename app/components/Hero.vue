<script setup>
import Stars from '~/components/Stars.vue'
</script>

<template>
  <section class="relative min-h-[720px] flex items-center overflow-hidden">

    <!-- ⭐ STARS -->
    <Stars />

    <div class="absolute inset-0 z-0">
      <img src="/hero-visual.png" alt="Hero Visual" class="
          w-full h-full object-cover
          object-right
          translate-x-[20%] md:translate-x-[35%]
          scale-110
          animate-[float_8s_ease-in-out_infinite]
        " />
      <div class="absolute inset-0 bg-gradient-to-r from-black/95 via-black/40 to-transparent"></div>
    </div>

    <!-- CONTENT -->
    <div class="relative z-10 max-w-7xl mx-auto px-6 py-28 w-full">
      <div class="grid md:grid-cols-2 gap-16 items-center">

        <div>
          <h1 class="text-6xl md:text-7xl font-extrabold leading-tight mb-6">
            Let’s build <br />
            <span class="text-purple-400">from here</span>
          </h1>

          <p class="text-xl text-gray-300 max-w-lg mb-10">
            Qubyn Infotech delivers secure, scalable, and high-performance
            software solutions designed for growth-driven companies.
          </p>

          <div class="flex flex-col sm:flex-row gap-4">
            <input type="email" placeholder="Enter your email" class="px-5 py-4 rounded-lg text-black w-full sm:w-80" />
            <button
              class="bg-purple-600 hover:bg-purple-500 px-5 py-2 rounded-lg">
              Get in Touch
            </button>
          </div>
        </div>

        <div class="hidden md:block"></div>
      </div>
    </div>

    <!-- BOTTOM FADE -->
    <div class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-to-b from-transparent to-[#0b0730]"></div>
  </section>
</template>
