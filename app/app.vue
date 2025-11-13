<script setup>
import { SpeedInsights } from "@vercel/speed-insights/nuxt"
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
      <client-only>
        <SpeedInsights />
      </client-only>
    </NuxtLayout>
  </div>
</template>