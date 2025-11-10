<template>
  <section
    id="contact"
    class="relative bg-layout-bg px-6 py-20 md:py-28 text-text-primary overflow-hidden"
  >
    <!-- BACKGROUND GLOW -->
    <div class="pointer-events-none absolute inset-0">
      <div class="absolute -top-32 left-1/2 -translate-x-1/2 w-[500px] h-[300px] bg-layout-surface/15 blur-[130px]"></div>
      <div class="absolute -bottom-32 right-1/2 translate-x-1/2 w-[520px] h-[280px] bg-bg-secondary/40 blur-[140px]"></div>
    </div>

    <div class="relative z-10 max-w-6xl mx-auto flex flex-col items-center text-center">
      <!-- HEADER / TEXT -->
      <p class="inline-flex items-center gap-2 text-xs font-semibold tracking-[0.2em] text-text-secondary uppercase mb-3">
        <span class="h-[1px] w-6 bg-text-secondary/60"></span>
        Contact
      </p>

      <h2 class="text-3xl md:text-4xl font-semibold tracking-tight leading-tight">
        Let’s <span class="text-text-secondary">connect</span> and create something meaningful
      </h2>

      <p class="mt-4 max-w-2xl text-sm md:text-base text-layout-surface/85">
        Terbuka untuk <span class="text-text-secondary font-medium">kerja sama profesional, proyek freelance, kolaborasi ide,</span>
        atau sekadar berdiskusi seputar pengembangan web dan teknologi.  
        Jangan ragu untuk menghubungi.
      </p>

      <!-- FORM -->
      <div
        class="mt-12 w-full rounded-xl bg-bg-primary/80 border border-layout-surface/40 shadow-[0_20px_55px_rgba(0,0,0,0.55)] p-6 md:p-8 backdrop-blur-sm"
      >
        <form @submit.prevent="handleSubmit" class="space-y-5 w-full">
          <!-- NAME -->
          <div class="space-y-1.5">
            <label class="block text-xs font-medium uppercase tracking-[0.16em] text-layout-surface/80 text-left">
              Your name
            </label>
            <input
              v-model="form.name"
              type="text"
              placeholder="e.g. John Doe"
              class="w-full rounded-xl bg-bg-primary/80 border border-layout-surface/40 px-3 py-2.5 text-sm text-text-primary placeholder:text-layout-surface/50 focus:outline-none focus:ring-2 focus:ring-text-secondary/80 focus:border-transparent"
            />
          </div>

          <!-- EMAIL -->
          <div class="space-y-1.5">
            <label class="block text-xs font-medium uppercase tracking-[0.16em] text-layout-surface/80 text-left">
              Your email
              <span class="text-layout-surface/60 normal-case text-[11px]">(optional, but useful)</span>
            </label>
            <input
              v-model="form.email"
              type="email"
              placeholder="you@example.com"
              class="w-full rounded-xl bg-bg-primary/80 border border-layout-surface/40 px-3 py-2.5 text-sm text-text-primary placeholder:text-layout-surface/50 focus:outline-none focus:ring-2 focus:ring-text-secondary/80 focus:border-transparent"
            />
          </div>

          <!-- SUBJECT -->
          <div class="space-y-1.5">
            <label class="block text-xs font-medium uppercase tracking-[0.16em] text-layout-surface/80 text-left">
              Subject
            </label>
            <select
              v-model="form.subject"
              class="w-full rounded-xl bg-bg-primary/80 border border-layout-surface/40 px-3 py-2.5 text-sm text-text-primary focus:outline-none focus:ring-2 focus:ring-text-secondary/80 focus:border-transparent"
            >
              <option value="Job opportunity">Job opportunity</option>
              <option value="Collaboration idea">Collaboration idea</option>
              <option value="Freelance project">Freelance project</option>
              <option value="Tech consultation">Tech consultation</option>
              <option value="Other">Other</option>
            </select>
          </div>

          <!-- MESSAGE -->
          <div class="space-y-1.5">
            <label class="block text-xs font-medium uppercase tracking-[0.16em] text-layout-surface/80 text-left">
              Message
            </label>
            <textarea
              v-model="form.message"
              rows="5"
              placeholder="Ceritakan sedikit tentang ide, proyek, atau kebutuhanmu — aku akan bantu melihat bagaimana bisa berkolaborasi."
              class="w-full rounded-xl bg-bg-primary/80 border border-layout-surface/40 px-3 py-2.5 text-sm text-text-primary placeholder:text-layout-surface/50 focus:outline-none focus:ring-2 focus:ring-text-secondary/80 focus:border-transparent resize-none"
            ></textarea>
          </div>

          <!-- PREVIEW -->
          <div class="space-y-2">
            <p class="text-xs font-medium uppercase tracking-[0.16em] text-layout-surface/80 text-left">
              Message preview
            </p>
            <div class="rounded-xl bg-bg-primary/90 border border-layout-surface/40 px-3 py-3 text-xs text-layout-surface/95 whitespace-pre-line">
              {{ previewMessage }}
            </div>
          </div>

          <!-- ACTION BUTTONS -->
          <div class="flex flex-wrap items-center gap-3 pt-3">
            <button
              type="button"
              @click="openWhatsApp"
              class="inline-flex items-center gap-2 rounded-full border border-text-secondary bg-text-secondary/80 px-5 py-2 text-sm font-medium text-text-primary hover:bg-text-secondary transition"
            >
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <line x1="22" y1="2" x2="11" y2="13"></line>
              <polygon points="22 2 15 22 11 13 2 9 22 2"></polygon>
            </svg>
              WhatsApp
            </button>
          </div>
        </form>
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
import { reactive, computed } from 'vue'

const props = defineProps({
  whatsappNumber: { type: String, default: '' },
  emailTo: { type: String, default: '' }
})

const form = reactive({
  name: '',
  email: '',
  subject: 'Job opportunity',
  message: '',
  channel: 'whatsapp'
})

const previewMessage = computed(() => {
  const lines = []
  lines.push(`Subject: ${form.subject}`)
  if (form.name) lines.push(`From: ${form.name}`)
  if (form.email) lines.push(`Email: ${form.email}`)
  lines.push('')
  lines.push('Message:')
  lines.push(form.message || '(tulis pesan di sini)')
  return lines.join('\n')
})

const buildWhatsAppUrl = () => {
  const base = 'https://wa.me/'
  const number = props.whatsappNumber || ''
  const text = encodeURIComponent(previewMessage.value)
  return `${base}${number}?text=${text}`
}

const openWhatsApp = () => window.open(buildWhatsAppUrl(), '_blank')
const handleSubmit = () => (form.channel === 'whatsapp' ? openWhatsApp() : '')
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