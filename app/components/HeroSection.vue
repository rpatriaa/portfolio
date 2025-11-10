<template>
  <section
    id="home"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-layout-bg text-white"
  >
    <!-- GLOW HIJAU KANAN & KIRI -->
    <div
      class="pointer-events-none absolute inset-0 opacity-80 mix-blend-screen"
    >
      <div
        class="absolute left-40 bottom-0 h-80 w-80 rounded-full bg-text-secondary blur-3xl"
      ></div>
      <div
        class="absolute right-40 top-0 h-96 w-96 rounded-full bg-text-secondary blur-3xl"
      ></div>
    </div>

    <!-- HURUF/SHAPE BESAR DI BELAKANG -->
    <div class="pointer-events-none absolute inset-0 text-9xl font-black text-emerald-900/10">
      <span class="absolute -left-10 top-1/4 select-none">e</span>
      <span class="absolute right-0 bottom-0 select-none">d</span>
    </div>

    <!-- SHAPE 3D PALSU (KURUNG KURAWAL, DLL) -->
    <div class="pointer-events-none absolute inset-0">
    <div
      class="floating-shape left-[15%] top-[10%] text-bg-primary"
      style="transform: perspective(1000px) rotateX(20deg) rotateY(-15deg)"
    >
      {
    </div>
    <div
      class="floating-shape right-[20%] top-[25%] text-bg-primary"
      style="transform: perspective(1000px) rotateX(-15deg) rotateY(25deg)"
    >
      #
    </div>
    <div
      class="floating-shape right-[15%] bottom-[15%] text-bg-primary"
      style="transform: perspective(1000px) rotateX(15deg) rotateY(-20deg)"
    >
      2
    </div>
  </div>

    <!-- KONTEN UTAMA -->
    <div class="relative z-10 max-w-4xl px-6 text-center">
      <p class="mb-4 text-sm tracking-[0.35em] text-text-primary uppercase">
        Home
      </p>

      <h1
        class="mb-6 text-4xl md:text-6xl font-semibold leading-tight tracking-tight text-text-primary"
      >
        Hi,
        I'm <span class="font-semibold">Patria</span>,
        a <span class="text-text-secondary">Web Developer</span> 
      </h1>

      <p
        class="mx-auto max-w-xl text-sm md:text-base leading-relaxed"
      >
        Blending backend logic and front-end design to build fast, functional, and beautiful web applications.
      </p>
    </div>

    <!-- SCROLL INDICATOR -->
    <div class="absolute bottom-8 left-1/2 -translate-x-1/2">
      <div class="h-10 w-px overflow-hidden bg-slate-700/60">
        <div class="animate-scroll-indicator h-full w-full bg-layout-surface"></div>
      </div>
    </div>
  </section>
</template>

<script setup>
// nggak butuh script dulu
</script>

<style scoped>
.floating-shape {
  @apply absolute text-6xl font-black;
  font-family: 'Courier New', monospace;
  animation: float 6s ease-in-out infinite alternate;
  
  /* Layered text shadow untuk efek 3D depth */
  text-shadow: 
    3px 3px 0px rgba(0, 0, 0, 0.2),
    6px 6px 0px rgba(0, 0, 0, 0.15),
    9px 9px 0px rgba(0, 0, 0, 0.1),
    12px 12px 0px rgba(0, 0, 0, 0.05),
    15px 15px 20px rgba(0, 0, 0, 0.3),
    -1px -1px 2px rgba(255, 255, 255, 0.5);
  
  filter: drop-shadow(0 10px 30px rgba(0, 0, 0, 0.3));
}


/* Animasi bentuk melayang */
@keyframes float {
  0%, 100% {
    transform: translateY(0px) translateX(0px);
  }
  50% {
    transform: translateY(-30px) translateX(20px);
  }
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
