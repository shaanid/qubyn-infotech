<script setup>
import { ref, onMounted } from 'vue'

const codeLines = [
  "export async function deployApp() {",
  "  await build()",
  "  await runTests()",
  "",
  "  await deployAPI()",
  "  await deployMobile()",
  "",
  "  console.log('Production is live!')",
  "}"
]

const displayedCode = ref("")
const lineIndex = ref(0)
const charIndex = ref(0)

const typingSpeed = 25 // lower = faster
const lineDelay = 300

const type = () => {
  if (lineIndex.value >= codeLines.length) return

  const line = codeLines[lineIndex.value]

  if (charIndex.value < line.length) {
    displayedCode.value += line.charAt(charIndex.value)
    charIndex.value++
    setTimeout(type, typingSpeed)
  } else {
    displayedCode.value += "\n"
    charIndex.value = 0
    lineIndex.value++
    setTimeout(type, lineDelay)
  }
}

onMounted(() => {
  type()
})
</script>

<template>
  <div class="code-card">
    <!-- HEADER -->
    <div class="code-header">
      <span class="dot red"></span>
      <span class="dot yellow"></span>
      <span class="dot green"></span>
      <span class="file-name">deploy.ts</span>
    </div>

    <!-- CODE -->
    <pre class="code-body"><code>{{ displayedCode }}</code></pre>
  </div>
</template>

<style scoped>
/* CARD */
.code-card {
  width: 100%;
  max-width: 460px;
  background: rgba(15, 15, 30, 0.85);
  backdrop-filter: blur(20px);
  border-radius: 18px;
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 0 90px rgba(140, 90, 255, 0.45);
  overflow: hidden;
}

/* HEADER */
.code-header {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 14px 16px;
  background: rgba(25, 25, 45, 0.9);
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
}

.red { background: #ff5f56 }
.yellow { background: #ffbd2e }
.green { background: #27c93f }

.file-name {
  margin-left: 12px;
  font-size: 13px;
  color: #c7c7ff;
}

/* CODE */
.code-body {
  padding: 22px;
  font-size: 14px;
  line-height: 1.7;
  color: #d6d6ff;
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
  white-space: pre-wrap;
  min-height: 220px;
}

/* CURSOR EFFECT */
.code-body::after {
  content: "▋";
  margin-left: 2px;
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50%, 100% { opacity: 1 }
  25%, 75% { opacity: 0 }
}
</style>
