<template>
  <div class="stars-wrapper">
    <div class="stars layer-back"></div>
    <div class="stars layer-front"></div>
  </div>
</template>

<style scoped>
.stars-wrapper {
  position: absolute;
  inset: 0;
  z-index: 6;
  pointer-events: none;
  overflow: hidden;
  mix-blend-mode: screen;
}

/* Common star layer */
.stars {
  position: absolute;
  inset: -60%;
  background-repeat: repeat;
  will-change: transform, opacity;
}

/* ⭐ BACK – SMALL STARS (SLOW FLOAT + SLOW TWINKLE) */
.layer-back {
  background-image:
    radial-gradient(1.5px 1.5px at 15% 25%, rgba(255,255,255,0.65) 50%, transparent 51%),
    radial-gradient(1.5px 1.5px at 35% 75%, rgba(210,190,255,0.6) 50%, transparent 51%),
    radial-gradient(1.5px 1.5px at 60% 45%, rgba(180,220,255,0.6) 50%, transparent 51%),
    radial-gradient(1.5px 1.5px at 85% 35%, rgba(255,255,255,0.65) 50%, transparent 51%);
  background-size: 220px 220px;
  opacity: 0.6;
  animation:
    stars-float-back 200s linear infinite,
    stars-twinkle-back 8s ease-in-out infinite;
}

/* ⭐ FRONT – BRIGHTER STARS (FASTER FLOAT + FASTER TWINKLE) */
.layer-front {
  background-image:
    radial-gradient(3px 3px at 25% 35%, rgba(255,255,255,0.95) 50%, transparent 51%),
    radial-gradient(3px 3px at 55% 20%, rgba(200,160,255,0.9) 50%, transparent 51%),
    radial-gradient(3px 3px at 80% 55%, rgba(140,200,255,0.9) 50%, transparent 51%);
  background-size: 360px 360px;
  opacity: 0.75;
  animation:
    stars-float-front 130s linear infinite,
    stars-twinkle-front 5s ease-in-out infinite;
}

/* 🌌 FLOATING (VERTICAL DRIFT) */
@keyframes stars-float-back {
  from { transform: translateY(0); }
  to   { transform: translateY(-520px); }
}

@keyframes stars-float-front {
  from { transform: translateY(0); }
  to   { transform: translateY(-380px); }
}

/* ✨ TWINKLING (BLINKING EFFECT) */
@keyframes stars-twinkle-back {
  0%, 100% {
    opacity: 0.55;
    transform: scale(1);
  }
  50% {
    opacity: 0.75;
    transform: scale(1.03);
  }
}

@keyframes stars-twinkle-front {
  0%, 100% {
    opacity: 0.65;
    transform: scale(1);
  }
  50% {
    opacity: 0.95;
    transform: scale(1.05);
  }
}
</style>
