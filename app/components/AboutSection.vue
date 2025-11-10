<template>
  <section
    id="about"
    class="relative min-h-screen bg-[#000000] text-white px-6 py-24 overflow-hidden flex flex-col"
  >
    <!-- BACKGROUND GLOW HALUS -->
    <div class="pointer-events-none absolute inset-0">
      <div class="absolute -top-24 left-1/2 -translate-x-1/2 w-[400px] h-[300px] bg-emerald-700/40 blur-[120px]"></div>
      <div class="absolute -bottom-24 left-1/2 -translate-x-1/2 w-[400px] h-[300px] bg-emerald-700/40 blur-[120px]"></div>
      <div class="absolute top-1/3 right-80 h-80 w-[500px] rounded-full bg-cyan-500/20 blur-3xl"></div>
    </div>

    <!-- WRAPPER KONTEN + MARQUEE -->
    <div class="relative z-10 max-w-6xl w-full mx-auto flex-1 flex flex-col justify-center items-center gap-16">
      <!-- KONTEN UTAMA (GRID TEKS + FOTO) -->
      <div
        class="grid gap-12 md:grid-cols-[minmax(0,1.4fr)_minmax(0,1fr)] items-center"
      >
        <!-- KIRI: TEKS -->
        <div class="text-justify">
          <p class="text-xs uppercase tracking-[0.35em] text-slate-400 mb-3">
            About Me
          </p>
          <h2 class="text-3xl md:text-4xl font-semibold mb-4">
            Rizki Patria Linaldi
          </h2>

          <p class="text-slate-300 text-sm md:text-base leading-relaxed mb-4">
            I’m a full-stack web developer who enjoys turning ideas into real, usable products.
            I work across the stack — from designing and optimizing database structures to building
            clean, modern interfaces that feel good to use.
          </p>

          <p class="text-slate-300 text-sm md:text-base leading-relaxed mb-6">
            Recently, I’ve been focusing on warehouse management systems using PHP OOP and MySQL, while exploring modern stacks like 
            Nuxt, Express, MongoDB, and SvelteKit in my personal projects. I care about code quality, performance, and keeping the UX simple and intuitive.
            I’m also open to working on diverse projects beyond my current scope and always eager to learn, adapt, and grow in new technical challenges.
          </p>

          <!-- HIGHLIGHT SKILLS / TAGS (STATIC) -->
          <div class="flex flex-wrap gap-2 mb-8">
            <span class="px-3 py-1 rounded-full bg-white/5 border border-slate-700 text-xs text-slate-200">
              Laravel · MySQL
            </span>
            <span class="px-3 py-1 rounded-full bg-white/5 border border-slate-700 text-xs text-slate-200">
              Nuxt · Tailwind
            </span>
          </div>

          <!-- SOCIAL ICONS -->
          <div class="flex items-center gap-4">
            <span class="text-xs uppercase tracking-[0.25em] text-slate-500">
              Find me on
            </span>

            <div class="flex items-center gap-3">
              <!-- GitHub -->
              <a
                href="https://github.com/rpatriaa/"
                target="_blank"
                rel="noopener noreferrer"
                class="group inline-flex h-9 w-9 items-center justify-center rounded-full border border-slate-700 bg-white/5 hover:border-emerald-400 hover:bg-emerald-400/10 transition-colors"
              >
                <svg
                  aria-hidden="true"
                  viewBox="0 0 24 24"
                  class="h-5 w-5 text-slate-300 group-hover:text-emerald-300 transition-colors"
                >
                  <path
                    fill="currentColor"
                    d="M12 2C6.48 2 2 6.58 2 12.26c0 4.51 2.87 8.33 6.84 9.68.5.1.68-.22.68-.49
                    0-.24-.01-.87-.01-1.71-2.78.62-3.37-1.37-3.37-1.37-.45-1.18-1.11-1.49-1.11-1.49-.91-.64.07-.63.07-.63
                    1 .07 1.53 1.06 1.53 1.06.9 1.57 2.36 1.12 2.94.86.09-.67.35-1.12.63-1.37-2.22-.26-4.56-1.14-4.56-5.08
                    0-1.12.39-2.03 1.03-2.75-.1-.26-.45-1.3.1-2.71 0 0 .84-.28 2.75 1.05A9.18 9.18 0 0 1 12 6.3c.85 0 1.7.12 2.5.34
                    1.9-1.33 2.74-1.05 2.74-1.05.55 1.41.21 2.45.1 2.71.64.72 1.03 1.63 1.03 2.75 0 3.95-2.34 4.81-4.57 5.07.36.32.68.94.68 1.9
                    0 1.37-.01 2.47-.01 2.81 0 .27.18.59.69.49A10.02 10.02 0 0 0 22 12.26C22 6.58 17.52 2 12 2Z"
                  />
                </svg>
                <span class="sr-only">GitHub</span>
              </a>

              <!-- LinkedIn -->
              <a
                href="https://www.linkedin.com/in/rizki-patria-linaldi/"
                target="_blank"
                rel="noopener noreferrer"
                class="group inline-flex h-9 w-9 items-center justify-center rounded-full border border-slate-700 bg-white/5 hover:border-emerald-400 hover:bg-emerald-400/10 transition-colors"
              >
                <svg
                  aria-hidden="true"
                  viewBox="0 0 24 24"
                  class="h-5 w-5 text-slate-300 group-hover:text-emerald-300 transition-colors"
                >
                  <path
                    fill="currentColor"
                    d="M6.09 6.5A2.09 2.09 0 1 1 2 6.5 2.09 2.09 0 0 1 6.09 6.5ZM2.34 8.91h3.5V21.5h-3.5ZM9.16 8.91h3.35v1.71h.05a3.67 3.67 0 0 1 3.3-1.81c3.53 0 4.18 2.32 4.18 5.33v7.36h-3.5v-6.53c0-1.56 0-3.57-2.18-3.57s-2.51 1.71-2.51 3.46v6.64h-3.5Z"
                  />
                </svg>
                <span class="sr-only">LinkedIn</span>
              </a>

              <!-- Instagram -->
              <a
                href="https://www.instagram.com/rizkipl12"
                target="_blank"
                rel="noopener noreferrer"
                class="group inline-flex h-9 w-9 items-center justify-center rounded-full border border-slate-700 bg-white/5 hover:border-emerald-400 hover:bg-emerald-400/10 transition-colors"
              >
                <svg
                  aria-hidden="true"
                  viewBox="0 0 24 24"
                  class="h-5 w-5 text-slate-300 group-hover:text-emerald-300 transition-colors"
                >
                  <path
                    fill="currentColor"
                    d="M12 7.35A4.65 4.65 0 1 0 16.65 12 4.65 4.65 0 0 0 12 7.35Zm0 7.65A3 3 0 1 1 15 12a3 3 0 0 1-3 3Zm5.88-7.81a1.09 1.09 0 1 1-1.09-1.09 1.09 1.09 0 0 1 1.09 1.09ZM21 8.58a6.59 6.59 0 0 0-1.79-4.67A6.59 6.59 0 0 0 14.54 2H9.46A6.59 6.59 0 0 0 4.79 3.91 6.59 6.59 0 0 0 3 8.58v5.08a6.59 6.59 0 0 0 1.79 4.67A6.59 6.59 0 0 0 9.46 20h5.08a6.59 6.59 0 0 0 4.67-1.79A6.59 6.59 0 0 0 21 13.66Zm-1.65 5a4.87 4.87 0 0 1-1.31 3.45 4.87 4.87 0 0 1-3.45 1.31H9.46a4.87 4.87 0 0 1-3.45-1.31 4.87 4.87 0 0 1-1.31-3.45V8.58a4.87 4.87 0 0 1 1.31-3.45A4.87 4.87 0 0 1 9.46 3.82h5.08a4.87 4.87 0 0 1 3.45 1.31 4.87 4.87 0 0 1 1.31 3.45Z"
                  />
                </svg>
                <span class="sr-only">Instagram</span>
              </a>

              <!-- Email -->
              <a
                href="mailto:rpatria04@gmail.com"
                class="group inline-flex h-9 w-9 items-center justify-center rounded-full border border-slate-700 bg-white/5 hover:border-emerald-400 hover:bg-emerald-400/10 transition-colors"
              >
                <svg
                  aria-hidden="true"
                  viewBox="0 0 24 24"
                  class="h-5 w-5 text-slate-300 group-hover:text-emerald-300 transition-colors"
                >
                  <path
                    fill="currentColor"
                    d="M4 5h16a2 2 0 0 1 2 2v10a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V7a2 2 0 0 1 2-2Zm0 2v.22l8 4.89 8-4.89V7Zm0 2.64V17h16v-7.36l-7.42 4.53a2 2 0 0 1-2.16 0Z"
                  />
                </svg>
                <span class="sr-only">Email</span>
              </a>
            </div>
          </div>
        </div>

        <!-- KANAN: FOTO -->
        <div class="flex justify-center md:justify-end">
          <div
            class="relative h-64 w-64 md:h-96 md:w-auto rounded-[2rem] bg-gradient-to-b from-slate-900 to-slate-950 shadow-[0_20px_60px_rgba(0,0,0,0.8)] overflow-hidden"
          >
            <img
              src="/profile.png"
              alt="Rizki Patria Linaldi"
              class="relative h-full w-full object-contain"
            />
          </div>
        </div>
      </div>

      <!-- MARQUEE SKILL ICONS (DI BAWAH KONTEN) -->
      <div class="relative w-full">
        <p class="text-xs uppercase tracking-[0.35em] text-slate-500 mb-4">
          Skills & Tools
        </p>

        <div class="marquee border-y border-slate-800/60 py-3 overflow-hidden">
          <div class="marquee-track flex items-center gap-10">
            <!-- list 1 -->
            <div
              v-for="skill in skills"
              :key="skill.name"
              class="marquee-item flex items-center gap-2 text-slate-200/90"
            >
              <img
                :src="skill.icon"
                :alt="skill.name + ' icon'"
                class="h-6 w-6"
                loading="lazy"
              />
              <span class="text-sm">{{ skill.name }}</span>
            </div>
            <!-- duplicate list 2 (buat loop halus) -->
            <div
              v-for="skill in skills"
              :key="'dup-' + skill.name"
              class="marquee-item flex items-center gap-2 text-slate-200/90"
            >
              <img
                :src="skill.icon"
                :alt="skill.name + ' icon'"
                class="h-6 w-6"
                loading="lazy"
              />
              <span class="text-sm">{{ skill.name }}</span>
            </div>
          </div>
        </div>
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

<script setup>
const skills = [
  { name: 'Nuxt.js', icon: '/icons/nuxt.svg' },
  { name: 'Vue.js', icon: '/icons/vue.svg' },
  { name: 'Tailwind CSS', icon: '/icons/tailwindcss.svg' },
  { name: 'Laravel', icon: '/icons/laravel.svg' },
  { name: 'MySQL', icon: '/icons/mysql.svg' },
  { name: 'Node.js', icon: '/icons/nodejs.svg' },
  { name: 'JavaScript', icon: '/icons/javascript.svg' },
  { name: 'Bootstrap', icon: '/icons/bootstrap.svg' },
  { name: 'Git', icon: '/icons/git.svg' },
]
</script>

<style scoped>
section {
  scroll-margin-top: 80px;
}

/* Animasi marquee custom */
@keyframes marquee-move {
  0% {
    transform: translateX(0);
  }
  100% {
    /* geser setengah lebar track karena kita duplikasi list */
    transform: translateX(-50%);
  }
}

.marquee-track {
  animation: marquee-move 22s linear infinite;
  width: max-content;
}

/* Pause saat hover */
.marquee:hover .marquee-track {
  animation-play-state: paused;
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
