<template>
  <section id="projects" class="relative bg-layout-bg text-text-primary px-6 py-20 md:py-24 overflow-hidden">
    <!-- BACKGROUND GLOW -->
    <div class="pointer-events-none absolute inset-0">
      <div class="absolute -top-32 left-1/2 -translate-x-1/2 w-[560px] h-[320px] bg-layout-surface/10 blur-[140px]">
      </div>
      <div class="absolute -bottom-36 right-10 w-[480px] h-[260px] bg-bg-secondary/40 blur-[130px]"></div>
      <div class="absolute inset-0 bg-[radial-gradient(circle_at_top,_rgba(255,255,255,0.06),_transparent_60%)]"></div>
    </div>

    <div class="max-w-6xl mx-auto">
      <!-- HEADER -->
      <header class="flex flex-col md:flex-row md:items-end md:justify-between gap-6 mb-10 md:mb-12">
        <div>
          <p
            class="inline-flex items-center gap-2 text-xs font-semibold tracking-[0.2em] text-text-secondary uppercase">
            <span class="h-[1px] w-6 bg-text-secondary/60"></span>
            Project Gallery
          </p>
          <h2 class="mt-4 text-3xl md:text-4xl font-semibold tracking-tight">
            Explore my
            <span
              class="bg-gradient-to-r from-text-secondary via-layout-surface to-text-primary bg-clip-text text-transparent">
              recent work
            </span>
          </h2>
          <p class="mt-3 max-w-2xl text-sm md:text-base text-layout-surface">
            Kumpulan project yang saya kerjakan: sistem internal, portfolio CMS,
            dan eksperimen teknologi untuk melatih skill fullstack dan
            arsitektur yang rapi.
          </p>
        </div>

        <div class="text-xs md:text-sm text-layout-surface">
          <div class="flex items-center gap-2">
            <span class="inline-flex h-2 w-2 rounded-full bg-text-secondary animate-pulse"></span>
            <span>Available for collaboration & freelance work</span>
          </div>
        </div>
      </header>

      <!-- GRID PROJECT -->
      <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-2">
        <div class="w-full rounded overflow-hidden shadow-lg bg-bg-secondary">
          <img class="w-full" src="/images/projects/casaaisha.webp" alt="Sunset in the mountains">
          <div class="px-6 py-4">
            <div class="font-bold text-xl text-text-secondary mb-2">Casa Aisha Landing Page</div>
            <p class="text-text-primary text-base">
                Landing page yang didesain untuk memasarkan dan mempromosikan properti hunian.
            </p>
            <div class="mt-4 flex items-center space-x-2 justify-between">
              <a href="https://casaaisha.com/" 
               class="inline-flex items-center gap-2 text-layout-surface hover:text-text-primary transition-colors duration-300"
               target="_blank"
               rel="noopener noreferrer">
              <span>Visit Website</span>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
              </svg>
              </a>
              <a href="https://github.com/rpatriaa/Compro-casaaisha" 
               class="inline-flex items-center gap-2 text-layout-surface hover:text-text-primary transition-colors duration-300"
               target="_blank"
               rel="noopener noreferrer">
              <span>Source Code</span>
              </a>
            </div>
          </div>
        </div>
        <div class="w-full rounded overflow-hidden shadow-lg bg-bg-secondary">
          <img class="w-full" src="/images/projects/portfolio-tailwindcss.webp" alt="Sunset in the mountains">
          <div class="px-6 py-4">
            <div class="font-bold text-xl text-text-secondary mb-2">Portfolio TailwindCss</div>
            <p class="text-text-primary text-base">
              Project portfolio untuk mengimplementasikan dan melatih pemahaman HTML, CSS, dan TailwindCSS. Dibuat dengan mengikuti tutorial dari Pak Sandhika Galih.
            </p>
            <div class="mt-4 flex items-center space-x-2 justify-between">
              <a href="https://casaaisha.com/" 
               class="inline-flex items-center gap-2 text-layout-surface hover:text-text-primary transition-colors duration-300"
               target="_blank"
               rel="noopener noreferrer">
              <span>Visit Website</span>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
              </svg>
              </a>
              <a href="https://github.com/rpatriaa/Compro-casaaisha" 
               class="inline-flex items-center gap-2 text-layout-surface hover:text-text-primary transition-colors duration-300"
               target="_blank"
               rel="noopener noreferrer">
              <span>Source Code</span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="w-full mx-auto">
      <!-- CLIENTS SECTION -->
      <div class="mt-24 border-t border-layout-surface/50 pt-12 text-center">
        <h3 class="text-2xl font-semibold text-text-primary mb-6">
          Clients I’ve worked with
        </h3>

        <div class="flex flex-wrap items-center justify-center gap-6 md:gap-10">
          <div class="group flex items-center gap-3 px-4 py-3">
            <img src="/images/clients/logo-casaaisha.png" class="h-40 w-80 object-contain rounded-md opacity-90 group-hover:opacity-100" />
            <span class="text-sm md:text-base font-medium text-text-primary">
            </span>
          </div>
          <div class="group flex items-center gap-3 px-4 py-3">
            <img src="/images/clients/gunadarma.png" class="h-40 w-40 object-contain rounded-md opacity-90 group-hover:opacity-100" />
            <span class="text-sm md:text-base font-medium text-text-primary">
            </span>
          </div>
        </div>
      </div>
    </div>

    <div class="w-full mx-auto">
      <div class="mt-24 border-t border-layout-surface/50 pt-12 text-end">
        <h3 class="text-2xl font-semibold text-text-primary mb-6">
          Certifications & Partnerships
        </h3>
        <div class="grid grid-cols-1 gap-4 sm:grid-cols-2 md:grid-cols-3">
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://images.unsplash.com/photo-1499696010180-025ef6e1a8f9?ixlib=rb-4.0.3&amp;ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&amp;auto=format&amp;fit=crop&amp;w=1470&amp;q=80"
              alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://images.unsplash.com/photo-1432462770865-65b70566d673?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&amp;ixlib=rb-1.2.1&amp;auto=format&amp;fit=crop&amp;w=1950&amp;q=80"
              alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://images.unsplash.com/photo-1497436072909-60f360e1d4b1?ixlib=rb-4.0.3&amp;ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&amp;auto=format&amp;fit=crop&amp;w=2560&amp;q=80"
              alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://images.unsplash.com/photo-1493246507139-91e8fad9978e?ixlib=rb-4.0.3&amp;ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&amp;auto=format&amp;fit=crop&amp;w=2940&amp;q=80"
              alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://images.unsplash.com/photo-1518623489648-a173ef7824f3?ixlib=rb-4.0.3&amp;ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&amp;auto=format&amp;fit=crop&amp;w=2762&amp;q=80"
              alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://images.unsplash.com/photo-1682407186023-12c70a4a35e0?ixlib=rb-4.0.3&amp;ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&amp;auto=format&amp;fit=crop&amp;w=2832&amp;q=80"
              alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://demos.creative-tim.com/material-kit-pro/assets/img/examples/blog5.jpg" alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://material-taillwind-pro-ct-tailwind-team.vercel.app/img/content2.jpg" alt="gallery-photo" />
          </div>
          <div>
            <img class="object-cover object-center w-full h-40 max-w-full rounded-lg"
              src="https://images.unsplash.com/photo-1620064916958-605375619af8?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&amp;ixlib=rb-1.2.1&amp;auto=format&amp;fit=crop&amp;w=1493&amp;q=80"
              alt="gallery-photo" />
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

</script>

<style scoped>
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
