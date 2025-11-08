<template>
  <div class="wrapper">
    <Navbar />
    <main>
      <slot />
    </main>
  </div>
</template>

<script setup>
import Navbar from '../app/components/Navbar.vue'
</script>

<style scoped>
.wrapper {
  min-height: 100vh;
  background: var(--layout-bg);
  transition: background 0.3s ease;
}

/* warna background per tema */
:root {
  --layout-bg: #f1f5f9;
}

.dark {
  --layout-bg: #020617;
}
</style>
