<script setup>
import Stars from '~/components/Stars.vue'
</script>

<template>
  <section class="relative min-h-[720px] flex items-center overflow-hidden">

    <!-- 🌍 IMAGE CONTAINER (RESPONSIVE + RIGHT-ALIGNED) -->
    <div class="
        absolute inset-y-0 right-0
        w-full
        max-w-[1400px]
        2xl:max-w-[1200px]

        z-[1]

        /* RESPONSIVE POSITIONING */
        translate-x-0
        sm:translate-x-12
        md:translate-x-28
        lg:translate-x-44

        /* RESPONSIVE SCALING */
        scale-[1.05]
        lg:scale-[1.03]
        2xl:scale-[1]

        transition-transform duration-[1200ms] ease-out
        will-change-transform
      ">
      <img src="/home-image.png" alt="Hero Visual" class="
          w-full h-full
          object-cover
          object-right
          animate-[float_16s_ease-in-out_infinite]
        " draggable="false" />
    </div>

    <!-- 🌫 DARK GRADIENT OVER IMAGE -->
    <div class="
        absolute inset-0 z-[2]
        bg-gradient-to-r
        from-black/90 via-black/55 to-transparent
      "></div>

    <!-- ⭐ STARS (VISIBLE ABOVE GRADIENT) -->
    <Stars />

    <!-- 📝 HERO CONTENT -->
    <div class="relative z-10 max-w-7xl mx-auto px-6 py-28 w-full">
      <div class="grid md:grid-cols-2 gap-16 items-center">

        <!-- TEXT COLUMN -->
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
            <input type="email" placeholder="Enter your email" class="
                px-5 py-4 rounded-xl
                bg-white/5 backdrop-blur-md
                border border-white/10
                text-white
                w-full sm:w-80
                focus:outline-none
                focus:ring-2 focus:ring-purple-500/50
                focus:border-purple-500/50
                placeholder:text-gray-500
                transition-all
              " />

            <button class="bg-purple-600 hover:bg-purple-500 px-5 py-2 rounded-lg">
              Get in Touch
            </button>
          </div>
        </div>

        <!-- EMPTY COLUMN (KEEPS LAYOUT BALANCE) -->
        <div class="hidden md:block"></div>
      </div>
    </div>

    <!-- 🔻 BOTTOM FADE -->
    <div class="
        absolute bottom-0 left-0 right-0
        z-[4] h-40
        bg-gradient-to-b from-transparent to-[#0b0730]
      "></div>

  </section>
</template>
