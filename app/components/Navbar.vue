<template>
  <header class="absolute top-0 left-0 w-full z-50">
    <div
      class="w-full flex items-center gap-4 md:gap-6 lg:gap-8
             px-4 sm:px-6 lg:px-12 h-20 sm:h-22 md:h-24"
    >
      <!-- Logo - Professional sizing -->
      <NuxtLink to="/" class="flex items-center flex-shrink-0">
        <img
          src="/white-logo-1.png"
          alt="Qubyn Infotech Logo"
          class="h-14 sm:h-16 md:h-20 w-auto object-contain"
        />
      </NuxtLink>


      <!-- Desktop Navigation - Centered between logo and button -->
      <nav class="hidden lg:flex items-center gap-8 xl:gap-10 text-gray-300 font-medium text-[15px] flex-1 justify-center">
        <NuxtLink to="/#services" class="hover:text-white transition-colors duration-200 cursor-pointer whitespace-nowrap">Services</NuxtLink>
        <NuxtLink to="/#solutions" class="hover:text-white transition-colors duration-200 cursor-pointer whitespace-nowrap">Solutions</NuxtLink>
        <NuxtLink to="/about" class="hover:text-white transition-colors duration-200 cursor-pointer whitespace-nowrap">About</NuxtLink>
        <NuxtLink to="/contact" class="hover:text-white transition-colors duration-200 cursor-pointer whitespace-nowrap">Contact</NuxtLink>
      </nav>

      <!-- Desktop CTA Button -->
      <button
        class="hidden lg:flex bg-purple-600 hover:bg-purple-500 transition-all duration-200
               px-6 py-2.5 rounded-lg font-semibold text-white text-sm flex-shrink-0
               shadow-lg shadow-purple-600/30 hover:shadow-purple-500/40"
      >
        Get Started
      </button>

      <!-- Mobile Menu Button -->
      <button
        @click="mobileMenuOpen = !mobileMenuOpen"
        class="lg:hidden flex items-center justify-center w-10 h-10 text-white hover:text-purple-400 transition-colors ml-auto"
        aria-label="Toggle menu"
      >
        <svg v-if="!mobileMenuOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
        <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
        </svg>
      </button>
    </div>

    <!-- Mobile Menu Overlay -->
    <Transition
      enter-active-class="transition-all duration-300 ease-out"
      enter-from-class="opacity-0 translate-y-[-20px]"
      enter-to-class="opacity-100 translate-y-0"
      leave-active-class="transition-all duration-200 ease-in"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 translate-y-[-20px]"
    >
      <div
        v-if="mobileMenuOpen"
        class="lg:hidden absolute top-full left-0 w-full bg-black/95 backdrop-blur-lg border-t border-purple-600/20"
      >
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 py-6 flex flex-col gap-4">
          <NuxtLink
            to="/#services"
            @click="mobileMenuOpen = false"
            class="text-gray-300 hover:text-white transition-colors duration-200 py-3 px-4 rounded-lg hover:bg-purple-600/10"
          >
            Services
          </NuxtLink>
          <NuxtLink
            to="/#solutions"
            @click="mobileMenuOpen = false"
            class="text-gray-300 hover:text-white transition-colors duration-200 py-3 px-4 rounded-lg hover:bg-purple-600/10"
          >
            Solutions
          </NuxtLink>
          <NuxtLink
            to="/about"
            @click="mobileMenuOpen = false"
            class="text-gray-300 hover:text-white transition-colors duration-200 py-3 px-4 rounded-lg hover:bg-purple-600/10"
          >
            About
          </NuxtLink>
          <NuxtLink
            to="/contact"
            @click="mobileMenuOpen = false"
            class="text-gray-300 hover:text-white transition-colors duration-200 py-3 px-4 rounded-lg hover:bg-purple-600/10"
          >
            Contact
          </NuxtLink>
          <button
            class="bg-purple-600 hover:bg-purple-500 transition-all duration-200
                   px-6 py-3 rounded-lg font-semibold text-white text-sm
                   shadow-lg shadow-purple-600/30 hover:shadow-purple-500/40 mt-2"
          >
            Get Started
          </button>
        </nav>
      </div>
    </Transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)
</script>
