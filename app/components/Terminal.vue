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
    <div class="glow-secondary"></div>

    <div class="workflow-panel">
      <div class="editor-container">
        <div class="panel-header">
          <div class="window-controls">
            <span class="dot red"></span>
            <span class="dot yellow"></span>
            <span class="dot green"></span>
          </div>
          <span class="file-name">server.js — node.js</span>
        </div>

        <div class="code-editor">
          <div class="line-numbers">
            <div v-for="n in 13" :key="n" class="ln">{{ n }}</div>
          </div>
          <div class="code-content">
            <div
              v-for="(line, index) in displayedLines"
              :key="index"
              class="code-line"
            >
              <span :style="{ color: line.color }">{{ line.text }}</span>
              <span v-if="index === currentLineIndex" class="cursor">|</span>
            </div>
            <div v-if="currentLineIndex >= codeLines.length" class="code-line">
              <span class="cursor">|</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=JetBrains+Mono&display=swap");

.workflow-wrapper {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 80px 20px;
  width: 100%;
}

.glow-outer {
  position: absolute;
  width: 800px;
  height: 800px;
  background: radial-gradient(
    circle at center,
    rgba(139, 92, 246, 0.2) 0%,
    rgba(37, 38, 94, 0.1) 40%,
    transparent 70%
  );
  filter: blur(80px);
  z-index: 0;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.glow-secondary {
  position: absolute;
  width: 600px;
  height: 600px;
  background: radial-gradient(
    circle at center,
    rgba(29, 78, 216, 0.15) 0%,
    transparent 60%
  );
  filter: blur(100px);
  z-index: 0;
  top: 30%;
  right: -10%;
}

/* Glass Background Panel */
.workflow-panel {
  position: relative;
  z-index: 1;
  width: 100%;
  max-width: 600px;
  height: 450px;
  display: flex;
  flex-direction: column;
  background: rgba(15, 15, 20, 0.7);
  backdrop-filter: blur(30px) saturate(160%);
  -webkit-backdrop-filter: blur(30px) saturate(160%);
  border-radius: 24px;
  padding: 20px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 40px 100px rgba(0, 0, 0, 0.5);
}

/* Bot Identity Styling */
.bot-header {
  margin-bottom: 24px;
  font-family: "Inter", sans-serif;
}

.bot-identity {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 10px;
}

.bot-icon {
  background: #312e81;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
}

.bot-name {
  color: #fff;
  font-weight: 500;
  font-size: 15px;
}

.bot-tag {
  background: rgba(255, 255, 255, 0.1);
  font-size: 11px;
  padding: 2px 6px;
  border-radius: 4px;
  color: #a1a1aa;
  margin-left: 6px;
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.bot-desc {
  color: #9494a3;
  font-size: 14px;
  line-height: 1.6;
}

/* Your Original Editor Design */
.editor-container {
  background: rgba(13, 17, 23, 0.9);
  border-radius: 12px;
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.05);
  flex: 1;
  display: flex;
  flex-direction: column;
}

.panel-header {
  display: flex;
  align-items: center;
  padding: 8px 16px;
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
.red {
  background: #ff5f56;
}
.yellow {
  background: #ffbd2e;
}
.green {
  background: #27c93f;
}

.file-name {
  margin-left: 20px;
  font-size: 12px;
  color: #7d8590;
  font-family: "JetBrains Mono", monospace;
}

.code-editor {
  display: flex;
  padding: 12px;
  font-family: "JetBrains Mono", monospace;
  font-size: 14px;
  line-height: 1.6;
  flex: 1;
  overflow-y: auto;
}

.line-numbers {
  text-align: right;
  padding-right: 20px;
  color: #3b424d;
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

@keyframes blink {
  50% {
    opacity: 0;
  }
}

@media (max-width: 600px) {
  .workflow-panel {
    padding: 16px;
  }
  .line-numbers {
    display: none;
  }
  .code-editor {
    font-size: 12px;
  }
}
</style>
