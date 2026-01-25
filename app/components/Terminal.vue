<script setup>
import { ref, onMounted } from "vue";

const codeLines = [
  { text: "const QubynInfotech = {", color: "#79c0ff" },
  {
    text: '  mission: "Empowering innovation through code",',
    color: "#a5d6ff",
  },
  { text: "  services: [", color: "#79c0ff" },
  { text: '    "Bespoke Web Solutions",', color: "#a5d6ff" },
  { text: '    "AI & Cloud Engineering",', color: "#a5d6ff" },
  { text: '    "Digital Transformation"', color: "#a5d6ff" },
  { text: "  ],", color: "#79c0ff" },
  { text: '  focus: "Visual Excellence & Scalability",', color: "#a5d6ff" },
  { text: '  approach: "User-centric design systems",', color: "#a5d6ff" },
  { text: '  results: "High-performance digital products"', color: "#a5d6ff" },
  { text: "};", color: "#79c0ff" },
  { text: "", color: "" },
  { text: 'Qubyn.build({ dream: "Your Future" });', color: "#d2a8ff" },
];

const displayedLines = ref([]);
const currentLineIndex = ref(0);
const currentCharIndex = ref(0);

const typeCode = () => {
  if (currentLineIndex.value < codeLines.length) {
    const currentLine = codeLines[currentLineIndex.value];

    if (displayedLines.value[currentLineIndex.value] === undefined) {
      displayedLines.value.push({ text: "", color: currentLine.color });
    }

    if (currentCharIndex.value < currentLine.text.length) {
      displayedLines.value[currentLineIndex.value].text +=
        currentLine.text[currentCharIndex.value];
      currentCharIndex.value++;
      setTimeout(typeCode, 30 + Math.random() * 50);
    } else {
      currentLineIndex.value++;
      currentCharIndex.value = 0;
      setTimeout(typeCode, 200);
    }
  }
};

onMounted(() => {
  typeCode();
});
</script>

<template>
  <div class="workflow-wrapper">
    <div class="glow-outer"></div>
    <div class="workflow-panel">
      <div class="glass-border"></div>

      <!-- HEADER -->
      <div class="panel-header">
        <div class="window-controls">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
        </div>
        <span class="file-name">server.js — node.js</span>
      </div>

      <!-- CODE CONTENT -->
      <div class="code-editor">
        <div class="line-numbers">
          <div v-for="n in 12" :key="n" class="ln">{{ n }}</div>
        </div>
        <div class="code-content">
          <div
            v-for="(line, index) in displayedLines"
            :key="index"
            class="code-line"
          >
            <span :style="{ color: line.color }">{{ line.text }}</span>
            <span
              v-if="
                index === currentLineIndex &&
                currentCharIndex < codeLines[currentLineIndex].text.length
              "
              class="cursor"
              >|</span
            >
          </div>
          <div v-if="currentLineIndex >= codeLines.length" class="code-line">
            <span class="cursor">|</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.workflow-wrapper {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  width: 100%;
}

.glow-outer {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  max-width: 700px;
  aspect-ratio: 1;
  background: radial-gradient(
    circle at center,
    rgba(147, 51, 234, 0.5) 0%,
    rgba(139, 92, 246, 0.3) 25%,
    rgba(124, 58, 237, 0.2) 45%,
    rgba(109, 40, 217, 0.1) 65%,
    transparent 85%
  );
  filter: blur(80px);
  pointer-events: none;
  z-index: 0;
}

.workflow-panel {
  position: relative;
  width: 100%;
  max-width: 630px;
  height: 430px;
  background: rgba(13, 17, 23, 0.9);
  backdrop-filter: blur(40px) saturate(200%);
  -webkit-backdrop-filter: blur(40px) saturate(200%);
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.6);
  z-index: 1;
  transition: all 0.3s ease;
}

.glass-border {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 20px;
  padding: 8px;
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.2) 0%,
    rgba(255, 255, 255, 0.05) 50%,
    rgba(255, 255, 255, 0.15) 100%
  );
  -webkit-mask:
    linear-gradient(#fff 0 0) content-box,
    linear-gradient(#fff 0 0);
  mask:
    linear-gradient(#fff 0 0) content-box,
    linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  pointer-events: none;
  z-index: 2;
}

.panel-header {
  display: flex;
  align-items: center;
  padding: 12px 20px;
  background: rgba(30, 36, 47, 0.4);
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.window-controls {
  display: flex;
  gap: 8px;
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
}

.red { background: #ff5f56; }
.yellow { background: #ffbd2e; }
.green { background: #27c93f; }

.file-name {
  margin-left: 20px;
  font-size: 13px;
  color: #7d8590;
  font-family: "JetBrains Mono", monospace;
}

.code-editor {
  display: flex;
  padding: 20px;
  font-family: "JetBrains Mono", "Fira Code", monospace;
  font-size: 14px;
  line-height: 1.6;
}

.line-numbers {
  text-align: right;
  padding-right: 20px;
  color: #30363d;
  user-select: none;
}

.code-content {
  flex: 1;
}

.code-line {
  white-space: pre;
}

.cursor {
  color: #bc8cff;
  animation: blink 1s step-end infinite;
}

@media (max-width: 768px) {
  .workflow-panel {
    height: 320px;
    border-radius: 12px;
  }
  
  .glass-border {
    border-radius: 12px;
    padding: 6px;
  }
  
  .code-editor {
    padding: 15px;
    font-size: 12px;
  }
  
  .line-numbers {
    padding-right: 15px;
  }
  
  .panel-header {
    padding: 10px 15px;
  }
  
  .file-name {
    margin-left: 15px;
    font-size: 11px;
  }
}

@media (max-width: 480px) {
  .workflow-panel {
    height: 280px;
  }
  
  .code-editor {
    padding: 10px;
    font-size: 11px;
  }
  
  .line-numbers {
    display: none;
  }
  
  .window-controls {
    gap: 6px;
  }
  
  .dot {
    width: 8px;
    height: 8px;
  }
}

@keyframes blink {
  from,
  to {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
}
</style>
