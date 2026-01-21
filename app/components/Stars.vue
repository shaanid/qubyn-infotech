<template>
  <div class="stars">
    <div class="stars-layer slow"></div>
    <div class="stars-layer fast"></div>
  </div>
</template>

<style scoped>
.stars {
  position: absolute;
  inset: 0;
  z-index: 1;
  pointer-events: none;
  overflow: hidden;
}

/* Shared */
.stars-layer {
  position: absolute;
  inset: -50%;
  background-repeat: repeat;
  will-change: transform;
}

/* Slow stars */
.slow {
  background-image:
    radial-gradient(2px 2px at 10% 20%, rgba(255,255,255,.9) 50%, transparent 51%),
    radial-gradient(1.5px 1.5px at 40% 80%, rgba(180,140,255,.8) 50%, transparent 51%),
    radial-gradient(1.2px 1.2px at 70% 40%, rgba(120,200,255,.7) 50%, transparent 51%);
  background-size: 350px 350px;
  opacity: 0.7;
  animation: stars-move 160s linear infinite;
}

/* Faster stars */
.fast {
  background-image:
    radial-gradient(1.5px 1.5px at 25% 35%, rgba(255,255,255,.9) 50%, transparent 51%),
    radial-gradient(1px 1px at 60% 70%, rgba(168,85,247,.8) 50%, transparent 51%);
  background-size: 250px 250px;
  opacity: 0.6;
  animation: stars-move 90s linear infinite;
}

@keyframes stars-move {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(-400px);
  }
}
</style>
