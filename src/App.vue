<script setup>
import { onBeforeUnmount, onMounted, ref } from 'vue'
import { RouterView } from 'vue-router'

const menuOpen = ref(false)
const scrolled = ref(false)
const handleScroll = () => { scrolled.value = window.scrollY > 24 }
const closeMenu = () => { menuOpen.value = false }

onMounted(() => {
  handleScroll()
  window.addEventListener('scroll', handleScroll, { passive: true })
})
onBeforeUnmount(() => window.removeEventListener('scroll', handleScroll))
</script>

<template>
  <div class="min-h-screen overflow-x-hidden bg-ink text-slate-100">
    <header class="fixed inset-x-0 top-0 z-50 transition-all duration-300" :class="scrolled ? 'border-b border-white/10 bg-ink/85 shadow-2xl shadow-black/20 backdrop-blur-xl' : 'bg-transparent'">
      <nav class="mx-auto flex max-w-7xl items-center justify-between px-5 py-4 lg:px-8" aria-label="Navigasi utama">
        <a href="#home" class="group flex items-center gap-3" @click="closeMenu">
          <span class="grid h-10 w-10 place-items-center rounded-xl border border-cyan-300/30 bg-cyan-300/10 font-display text-lg font-black text-cyan-300 transition group-hover:-rotate-6 group-hover:bg-cyan-300 group-hover:text-ink">F</span>
          <span class="font-display text-base font-extrabold tracking-wide">FAIZ<span class="text-cyan-300">.DEV</span></span>
        </a>
        <div class="hidden items-center gap-8 md:flex">
          <a v-for="item in ['Tentang', 'Keahlian', 'Proyek', 'Pengalaman', 'Kontak']" :key="item" :href="`#${item.toLowerCase()}`" class="nav-link">{{ item }}</a>
          <a href="/Profile.pdf" download class="rounded-full border border-cyan-300/40 px-5 py-2.5 text-sm font-bold text-cyan-200 transition hover:bg-cyan-300 hover:text-ink">Unduh CV</a>
        </div>
        <button class="grid h-10 w-10 place-items-center rounded-xl border border-white/10 md:hidden" :aria-expanded="menuOpen" aria-label="Buka menu" @click="menuOpen = !menuOpen">
          <svg class="h-5 w-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path v-if="!menuOpen" d="M4 7h16M4 12h16M4 17h16"/><path v-else d="m6 6 12 12M18 6 6 18"/></svg>
        </button>
      </nav>
      <div v-if="menuOpen" class="border-t border-white/10 bg-ink/95 px-5 py-5 backdrop-blur-xl md:hidden">
        <a v-for="item in ['Tentang', 'Keahlian', 'Proyek', 'Pengalaman', 'Kontak']" :key="item" :href="`#${item.toLowerCase()}`" class="block border-b border-white/5 py-3 text-sm font-bold text-slate-300" @click="closeMenu">{{ item }}</a>
      </div>
    </header>
    <RouterView />
  </div>
</template>
