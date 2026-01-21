<template>
  <div class="min-h-screen bg-gradient-to-b from-[#05020d] via-[#0b0730] to-[#02010a] text-white overflow-x-hidden">
    <Navbar />
    <slot />
    <Footer />
  </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
</script>
