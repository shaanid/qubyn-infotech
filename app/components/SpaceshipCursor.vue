<template>
  <div
    class="spaceship-cursor"
    :style="style"
  >
    <img src="/spaceship.png" alt="Spaceship Cursor" />
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const mouse = { x: 0, y: 0 }
const pos = { x: 0, y: 0 }

const speed = 0.1 // smooth follow (lower = slower)

const style = ref({
  transform: 'translate3d(0, 0, 0)',
})

const animate = () => {
  pos.x += (mouse.x - pos.x) * speed
  pos.y += (mouse.y - pos.y) * speed

  style.value = {
    transform: `
      translate3d(${pos.x}px, ${pos.y}px, 0)
      translate(-50%, -50%)
    `,
  }

  requestAnimationFrame(animate)
}

const onMouseMove = (e) => {
  mouse.x = e.clientX
  mouse.y = e.clientY
}

onMounted(() => {
  window.addEventListener('mousemove', onMouseMove)
  animate()
})

onBeforeUnmount(() => {
  window.removeEventListener('mousemove', onMouseMove)
})
</script>

<style scoped>
.spaceship-cursor {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9999;
  pointer-events: none; /* IMPORTANT */
}

/* BIG ROUND SPACESHIP SIZE */
.spaceship-cursor img {
  width: clamp(140px, 18vw, 210px); /* responsive BIG size */
  height: auto;
  filter: drop-shadow(0 0 35px rgba(160, 120, 255, 0.8));
}
</style>
