<template>
  <header class="navbar">
    <div class="navbar-inner">
      <!-- KIRI: Nama -->
      <div class="brand">
        <span class="brand-name">Rizki Patria</span>
      </div>

      <!-- TENGAH: Toggle Darkmode -->
      <div class="toggle-container">
        <label class="switch">
          <input type="checkbox" v-model="isDark" @change="toggleTheme" />
          <span class="slider"></span>
        </label>
      </div>

      <!-- KANAN: Menu -->
      <nav class="nav-links">
        <a href="#experience">Experience</a>
        <a href="#about">About Me</a>
        <a href="#project">Project</a>
        <a href="#contact">Contact Me</a>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref, watch } from 'vue'

// state dark mode
const isDark = ref(false)

const toggleTheme = () => {
  const html = document.documentElement
  if (isDark.value) {
    html.classList.add('dark')
  } else {
    html.classList.remove('dark')
  }
}

// simpan preferensi di localStorage
watch(isDark, (val) => {
  localStorage.setItem('theme', val ? 'dark' : 'light')
})

// pas awal load
if (process.client) {
  const saved = localStorage.getItem('theme')
  if (saved === 'dark') {
    isDark.value = true
    document.documentElement.classList.add('dark')
  }
}
</script>

<style scoped>
.navbar {
  position: sticky;
  top: 0;
  z-index: 50;
  backdrop-filter: blur(16px);
  background: var(--bg-color);
  transition: background 0.3s ease;
}

.navbar-inner {
  max-width: 1120px;
  margin: 0 auto;
  padding: 16px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: var(--text-color);
}

/* Nama kiri */
.brand-name {
  font-weight: 700;
  letter-spacing: 0.05em;
}

/* Menu kanan */
.nav-links {
  display: flex;
  gap: 24px;
  font-size: 14px;
}

.nav-links a {
  color: var(--text-muted);
  text-decoration: none;
  position: relative;
  transition: color 0.2s ease;
}

.nav-links a:hover {
  color: var(--accent);
}

/* Toggle di tengah */
.toggle-container {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}

/* switch toggle */
.switch {
  position: relative;
  display: inline-block;
  width: 44px;
  height: 22px;
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0; left: 0;
  right: 0; bottom: 0;
  background-color: #ccc;
  transition: .4s;
  border-radius: 34px;
}

.slider:before {
  position: absolute;
  content: "";
  height: 16px;
  width: 16px;
  left: 3px;
  bottom: 3px;
  background-color: white;
  transition: .4s;
  border-radius: 50%;
}

input:checked + .slider {
  background-color: #22c55e;
}

input:checked + .slider:before {
  transform: translateX(22px);
}

/* Warna tema */
:root {
  --bg-color: rgba(255, 255, 255, 0.8);
  --text-color: #111827;
  --text-muted: #4b5563;
  --accent: #22c55e;
}

.dark {
  --bg-color: rgba(2, 6, 23, 0.8);
  --text-color: #f9fafb;
  --text-muted: #9ca3af;
  --accent: #22c55e;
}
</style>
