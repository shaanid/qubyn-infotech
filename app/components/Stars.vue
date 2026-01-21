<template>
  <div class="absolute inset-0 z-[1] pointer-events-none">
    <span
      v-for="i in 50"
      :key="i"
      class="star"
      :style="randomStyle()"
    ></span>
  </div>
</template>

<script setup>
const randomStyle = () => {
  const size = Math.random() * 2 + 1
  const left = Math.random() * 100
  const top = Math.random() * 100
  const duration = Math.random() * 30 + 15
  const delay = Math.random() * 10

  return {
    width: `${size}px`,
    height: `${size}px`,
    left: `${left}%`,
    top: `${top}%`,
    animationDuration: `${duration}s`,
    animationDelay: `${delay}s`,
  }
}
</script>

<style>
.star {
  position: absolute;
  background: rgba(200, 200, 255, 0.8);
  border-radius: 9999px;
  animation:
    star-move linear infinite,
    star-fade ease-in-out infinite;
}

@keyframes star-move {
  from { transform: translateY(0); }
  to { transform: translateY(-120px); }
}

@keyframes star-fade {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.8; }
}
</style>
