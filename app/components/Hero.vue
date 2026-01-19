<template>
  <section class="relative overflow-hidden min-h-[600px] flex items-center">
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img src="/hero-visual.png" alt="Background" class="w-full h-full object-cover object-right md:object-center" />
      <!-- Gradient Overlay: Darker on left for text readability, clearer on right for image -->
      <div class="absolute inset-0 bg-gradient-to-r from-black/90 via-black/50 to-transparent"></div>
    </div>

    <div class="relative z-10 max-w-7xl mx-auto px-6 py-20 w-full">
      <div class="grid md:grid-cols-2 gap-12">
        <!-- Text Content on the Left -->
        <div class="max-w-2xl">
          <h2 class="text-5xl md:text-7xl font-extrabold leading-tight text-white mb-6">
            Let’s build<br />
            <span class="text-accent">from here</span>
          </h2>
          <p class="text-xl text-gray-200 max-w-lg mb-10 leading-relaxed">
            Qubyn Infotech delivers secure, scalable, and high-performance software
            solutions designed for growth-driven companies.
          </p>

          <div class="flex flex-col sm:flex-row gap-4">
            <input type="email" placeholder="Enter your email"
              class="px-5 py-4 rounded-lg text-black w-full sm:w-80 border-2 border-transparent focus:border-accent outline-none transition-all" />
            <button
              class="bg-blue-500 hover:bg-blue-100 text-white font-bold py-2 px-4 rounded-lg text-lg transition-all transform hover:scale-105">
              Get in Touch
            </button>
          </div>
        </div>

        <!-- Empty Right Column to push content left and reveal image -->
        <div class="hidden md:block"></div>
      </div>
    </div>
  </section>
</template>
