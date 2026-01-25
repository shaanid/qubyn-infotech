<template>
  <div class="min-h-screen text-white relative overflow-x-hidden bg-black" 
       style="background-image: 
         radial-gradient(at 0% 0%, rgba(20, 30, 80, 0.25) 0%, transparent 50%),
         radial-gradient(at 100% 100%, rgba(15, 25, 70, 0.2) 0%, transparent 50%),
         radial-gradient(at 50% 50%, rgba(10, 20, 60, 0.1) 0%, transparent 80%);">
    <!-- <SpaceshipCursor /> -->
    <Navbar />
    <slot />
    <Footer />
  </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
</script>
