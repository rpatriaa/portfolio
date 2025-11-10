<template>
  <section
    id="experience"
    class="relative min-h-screen text-white py-24 px-6 overflow-hidden"
  >
    <div class="absolute inset-0 bg-[#000000] z-5">
      <!-- Light gradient blobs -->
      <div class="absolute -top-10 -left-40 w-[800px] h-[500px] bg-emerald-500/60 blur-[150px] animate-pulse-slow"></div>
      <div class="absolute top-1/3 right-0 w-[400px] h-[400px] bg-emerald-500/50 blur-[150px] animate-move-light"></div>

      <!-- subtle texture -->
      <div class="absolute inset-0 opacity-20 mix-blend-overlay bg-[url('https://www.transparenttextures.com/patterns/asfalt-dark.png')]"></div>
    </div>

    <!-- TITLE -->
    <div class="relative text-center mb-24 z-10">
      <h2 class="text-5xl md:text-6xl font-semibold mb-3 text-emerald-100 drop-shadow-[0_0_20px_rgba(16,185,129,0.2)]">
        Experience
      </h2>
      <p class="text-slate-400 text-base md:text-lg max-w-2xl mx-auto">
        A journey of growth through code, creativity, and collaboration.
      </p>
    </div>

    <!-- TIMELINE -->
    <div class="relative max-w-5xl mx-auto z-10">
      <div class="absolute left-1/2 top-0 bottom-0 w-[2px] bg-gradient-to-b from-emerald-500/40 to-transparent"></div>

      <!-- ITEM 1 -->
      <div class="relative mb-24 flex items-center justify-start md:justify-end">
        <div
          class="w-full md:w-1/2 bg-white/5 backdrop-blur-lg border border-emerald-800/30 rounded-2xl p-6 md:p-8 shadow-lg hover:shadow-[0_0_35px_-10px_rgba(16,185,129,0.6)] transition-transform duration-300 hover:-translate-y-1"
        >
          <h3 class="text-2xl font-semibold text-emerald-400 mb-2">
            Software Developer
          </h3>
          <p><span class="text-text-secondary">Full Time - WFO</span></p>
          <p class="text-sm text-slate-400 mb-4">
            Sistem Integrasi Indonesia ·  Nov 2024 – Present
          </p>
          <p class="text-slate-300 text-sm leading-relaxed">
            Developing and maintaining warehouse management systems with PHP and MySQL.  
            Improving backend performance and crafting efficient UI experiences for operations teams.
          </p>
        </div>
        <div
          class="absolute left-1/2 -translate-x-1/2 h-4 w-4 rounded-full bg-emerald-400 shadow-[0_0_25px_4px_rgba(16,185,129,0.7)]"
        ></div>
      </div>

      <!-- ITEM 2 -->
      <div class="relative mb-24 flex items-center justify-end md:justify-start">
        <div
          class="w-full md:w-1/2 bg-white/5 backdrop-blur-lg border border-emerald-800/30 rounded-2xl p-6 md:p-8 shadow-lg hover:shadow-[0_0_35px_-10px_rgba(16,185,129,0.6)] transition-transform duration-300 hover:-translate-y-1"
        >
          <h3 class="text-2xl font-semibold text-emerald-400 mb-2">
            Full-Stack Developer
          </h3>
          <p><span class="text-text-secondary">Internship - WFO</span></p>
          <p class="text-sm text-slate-400 mb-4">
            Vitech Asia ·  May 2024 – June 2024
          </p>
          <p class="text-slate-300 text-sm leading-relaxed">
            Building CMS using Laravel, Blade, and MySQL.  
            Experimenting with Laravel Blade for minimalist, scalable architectures.
          </p>
        </div>
        <div
          class="absolute left-1/2 -translate-x-1/2 h-4 w-4 rounded-full bg-emerald-400 shadow-[0_0_25px_4px_rgba(16,185,129,0.7)]"
        ></div>
      </div>

      <!-- ITEM 3 -->
      <div class="relative mb-12 flex items-center justify-start md:justify-end">
        <div
          class="w-full md:w-1/2 bg-white/5 backdrop-blur-lg border border-emerald-800/30 rounded-2xl p-6 md:p-8 shadow-lg hover:shadow-[0_0_35px_-10px_rgba(16,185,129,0.6)] transition-transform duration-300 hover:-translate-y-1"
        >
          <h3 class="text-2xl font-semibold text-emerald-400 mb-2">
            Assistant Ilab Gundarma
          </h3>
          <p><span class="text-text-secondary">Full-time - Hybrid</span></p>
          <p class="text-sm text-slate-400 mb-4">
            Gundarma University ·  Nov 2023 – June 2025
          </p>
          <p class="text-slate-300 text-sm leading-relaxed">
            Designed and supported database learning experiences for university students —
            guiding them through SQL Workbench with hands-on sessions, precise query testing, and structured academic feedback.
          </p>
        </div>
        <div
          class="absolute left-1/2 -translate-x-1/2 h-4 w-4 rounded-full bg-emerald-400 shadow-[0_0_25px_4px_rgba(16,185,129,0.7)]"
        ></div>
      </div>
    </div>

    <!-- SCROLL INDICATOR -->
    <div class="absolute bottom-8 left-1/2 -translate-x-1/2">
      <div class="h-10 w-px overflow-hidden bg-slate-700/60">
        <div class="animate-scroll-indicator h-full w-full bg-layout-surface"></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Animasi untuk cahaya bergerak */
@keyframes move-light {
  0% {
    transform: translate(0, 0);
  }
  50% {
    transform: translate(-30px, 40px);
  }
  100% {
    transform: translate(0, 0);
  }
}
@keyframes pulse-slow {
  0%, 100% {
    opacity: 0.3;
    transform: scale(1);
  }
  50% {
    opacity: 0.6;
    transform: scale(1.1);
  }
}
.animate-move-light {
  animation: move-light 6s ease-in-out infinite;
}
.animate-pulse-slow {
  animation: pulse-slow 8s ease-in-out infinite;
}

/* Biar scroll lebih halus */
section {
  scroll-margin-top: 80px;
}

/* Animasi garis scroll di bawah */
@keyframes scroll-indicator {
  0% {
    transform: translateY(-100%);
  }
  100% {
    transform: translateY(100%);
  }
}

.animate-scroll-indicator {
  animation: scroll-indicator 1.4s linear infinite;
}
</style>
