<template>
  <SpeedInsights />
  <div class="bg-layout-bg min-h-screen">
    <Navbar />
    <main>
      <slot />
    </main>
  </div>
</template>

<script setup>
import { SpeedInsights } from "@vercel/speed-insights/nuxt"
</script>

<style scoped>  

</style>