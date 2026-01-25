<script setup>
import {
    Zap,
    Smartphone,
    ShieldCheck,
    Rocket
} from 'lucide-vue-next'
</script>

<template>
    <div class="dev-section">
        <!-- LEFT CONTENT -->
        <div class="dev-left">
            <h2>Web & App Development</h2>
            <p class="subtitle">
                We build scalable, secure, and high-performance digital products
                using modern technologies and clean engineering practices.
            </p>

            <ul class="feature-list">
                <li>
                    <Zap class="icon" />
                    High-performance web applications
                </li>

                <li>
                    <Smartphone class="icon" />
                    Cross-platform mobile apps
                </li>

                <li>
                    <ShieldCheck class="icon" />
                    Secure backend & APIs
                </li>

                <li>
                    <Rocket class="icon" />
                    CI/CD & cloud deployment
                </li>
            </ul>
        </div>

        <!-- RIGHT CODE GLASS -->
       <TypingCode />

    </div>
</template>

<style scoped>
.dev-section {
    display: grid;
    grid-template-columns: 1.1fr 1fr;
    gap: 4rem;
    align-items: center;
    max-width: 1200px;
    margin: auto;
    padding: 4rem 2rem;
}

/* LEFT */
.dev-left h2 {
    font-size: 2.6rem;
    font-weight: 700;
    color: #ffffff;
}

.subtitle {
    margin-top: 1rem;
    color: #cfcfff;
    max-width: 520px;
    line-height: 1.6;
}

/* FEATURE LIST */
.feature-list {
    margin-top: 2.2rem;
    display: flex;
    flex-direction: column;
    gap: 1.3rem;
}

.feature-list li {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    color: #e5e5ff;
    font-size: 1rem;
}

/* ICON STYLE (PREMIUM) */
.icon {
    width: 18px;
    height: 18px;
    color: #a78bfa;
    filter: drop-shadow(0 0 8px rgba(167, 139, 250, 0.6));
}

/* RIGHT */
.dev-right {
    display: flex;
    justify-content: center;
}

/* CODE CARD */
.code-card {
    width: 100%;
    max-width: 460px;
    background: rgba(15, 15, 30, 0.8);
    backdrop-filter: blur(20px);
    border-radius: 18px;
    border: 1px solid rgba(255, 255, 255, 0.08);
    overflow: hidden;
}

/* HEADER */
.code-header {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 14px 16px;
    background: rgba(25, 25, 45, 0.85);
}

.dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
}

.red {
    background: #ff5f56
}

.yellow {
    background: #ffbd2e
}

.green {
    background: #27c93f
}

.file-name {
    margin-left: 12px;
    font-size: 13px;
    color: #c7c7ff;
}

/* CODE BODY */
.code-body {
    padding: 22px;
    font-size: 14px;
    line-height: 1.6;
    color: #d6d6ff;
    overflow-x: auto;
}

/* RESPONSIVE */
@media (max-width: 900px) {
    .dev-section {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .feature-list li {
        justify-content: center;
    }
}
</style>
