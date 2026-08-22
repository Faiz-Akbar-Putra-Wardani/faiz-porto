<script setup>
const skills = [
  { name: 'Laravel', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/laravel/laravel-original.svg', tone: 'from-rose-500/20 to-orange-500/5', border: 'border-rose-400/20' },
  { name: 'Next.js', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg', invert: true, tone: 'from-slate-300/15 to-transparent', border: 'border-slate-300/20' },
  { name: 'Node.js', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg', tone: 'from-lime-500/20 to-green-500/5', border: 'border-lime-400/20' },
  { name: 'Django', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/django/django-plain.svg', brighten: true, tone: 'from-emerald-500/20 to-teal-500/5', border: 'border-emerald-400/20' },
  { name: 'Python', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg', tone: 'from-sky-500/20 to-amber-500/5', border: 'border-sky-400/20' },
  { name: 'PHP', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/php/php-original.svg', tone: 'from-indigo-500/20 to-violet-500/5', border: 'border-indigo-400/20' },
  { name: 'JavaScript', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg', tone: 'from-yellow-400/20 to-amber-500/5', border: 'border-yellow-300/20' },
  { name: 'Vue.js', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original.svg', tone: 'from-emerald-500/20 to-cyan-500/5', border: 'border-emerald-400/20' },
  { name: 'React', logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg', tone: 'from-cyan-500/20 to-sky-500/5', border: 'border-cyan-400/20' },
]

const experiences = [
  { period: 'Apr 2026 — Sekarang', role: 'Web Developer', company: 'RS. Airan Raya', location: 'Lampung Selatan', current: true, description: 'Membangun dan mengembangkan solusi web yang mendukung kebutuhan operasional dan layanan rumah sakit.' },
  { period: 'Jul 2025 — Sep 2025', role: 'Web Developer Intern', company: 'PT Microdata Indonesia', location: 'Sukarame, Lampung', description: 'Mengembangkan landing page Next.js dengan backend Laravel, admin dashboard CMS, serta sistem manajemen pelanggan untuk penyedia layanan internet.' },
  { period: 'Des 2023 — Agu 2025', role: 'Web Development Tutor', company: 'UKM Programming Teknokrat', location: 'Bandar Lampung', description: 'Mengajar HTML, CSS, PHP Native, dan Laravel sekaligus mendampingi anggota membangun proyek web dan kemampuan problem-solving.' },
  { period: 'Mar 2024 — Feb 2025', role: 'Web Developer', company: 'Center of Excellence Software Development', location: 'Bandar Lampung', description: 'Berkolaborasi dalam merancang, mengimplementasikan, dan menguji fitur website yang aman, scalable, dan sesuai kebutuhan bisnis.' },
]

const certifications = ['Junior Web Developer — VSGA', 'Front-End Web untuk Pemula', 'Pemrograman PHP', 'Dasar Pemrograman Web']
</script>

<template>
  <main>
    <section id="home" class="hero-grid relative flex min-h-screen items-center overflow-hidden pt-24">
      <div class="orb orb-one"></div><div class="orb orb-two"></div>
      <div class="mx-auto grid w-full max-w-7xl items-center gap-4 px-5 pb-10 lg:grid-cols-[1.05fr_.95fr] lg:px-8">
        <div class="relative z-10 pt-12 lg:pt-0">
          <p class="mb-5 font-mono text-xs uppercase tracking-[.24em] text-cyan-300">Web Developer · Bandar Lampung</p>
          <h1 class="font-display text-5xl font-semibold leading-[.98] tracking-[-.055em] text-white sm:text-7xl xl:text-[5.25rem]">Faiz Akbar<br /><span class="text-slate-400">Putra Wardani.</span></h1>
          <p class="mt-7 max-w-xl text-lg leading-relaxed text-slate-400 sm:text-xl">Saya membangun antarmuka dan sistem web yang jelas, responsif, dan dapat dipelihara—dari pengalaman pengguna hingga layanan di baliknya.</p>
          <div class="mt-9 flex flex-wrap gap-4"><a href="#pengalaman" class="primary-btn">Lihat pengalaman <span aria-hidden="true">↘</span></a><a href="mailto:faizbot81@gmail.com" class="secondary-btn">Hubungi saya</a></div>
        </div>
        <div class="relative mx-auto mt-6 w-full max-w-[570px] self-end lg:mt-0">
          <div class="absolute inset-x-[14%] bottom-[8%] h-[60%] rounded-full bg-cyan-400/15 blur-[70px]"></div>
          <div class="character-frame relative">
            <img src="/images/faiz-anime-developer.png" alt="Ilustrasi anime Faiz sebagai web developer" class="relative z-10 mx-auto max-h-[76vh] w-full object-contain object-bottom" />
            <div class="float-card left-1 top-[28%] hidden sm:flex"><span class="text-cyan-300">&lt;/&gt;</span><div><b>Clean Code</b><small>Every commit counts</small></div></div>
            <div class="float-card right-0 top-[52%] hidden sm:flex"><span class="text-violet-300">⚡</span><div><b>Full Stack</b><small>Idea to production</small></div></div>
          </div>
        </div>
      </div>
      <a href="#tentang" class="absolute bottom-6 left-1/2 z-20 hidden -translate-x-1/2 flex-col items-center gap-2 text-[10px] font-bold uppercase tracking-[.25em] text-slate-500 lg:flex">Scroll <span class="h-8 w-px bg-gradient-to-b from-cyan-300 to-transparent"></span></a>
    </section>

    <section id="tentang" class="section-shell">
      <div class="grid gap-12 lg:grid-cols-[.75fr_1.25fr] lg:gap-20">
        <div><p class="eyebrow">01 — Profil</p><h2 class="section-title">Tentang saya.</h2><p class="mt-7 max-w-xs text-sm leading-7 text-slate-500">Lulusan Informatika, web developer, dan pengajar yang menikmati proses mengubah kebutuhan menjadi produk digital yang berguna.</p></div>
        <div class="glass-card p-7 sm:p-10">
          <p class="text-lg leading-8 text-slate-300">Saya adalah lulusan <b class="text-white">Informatika Universitas Teknokrat Indonesia</b> dengan minat kuat pada Web Development dan Software Engineering.</p>
          <p class="mt-5 leading-7 text-slate-400">Perjalanan saya berkembang lewat bootcamp, pembelajaran mandiri, mengajar, dan pengalaman industri. Saya terbiasa membangun aplikasi dari antarmuka hingga API—menggunakan HTML, CSS, JavaScript, PHP, Laravel, Express.js, dan teknologi web modern lainnya.</p>
          <p class="mt-5 leading-7 text-slate-400">Bagi saya, teknologi adalah cara mengubah masalah rumit menjadi pengalaman yang terasa sederhana bagi pengguna.</p>
          <div class="mt-8 border-t border-white/10 pt-6"><b class="block text-sm font-semibold text-white">Sarjana Informatika</b><span class="mt-1 block text-sm text-slate-500">Universitas Teknokrat Indonesia · 2026</span></div>
        </div>
      </div>
    </section>

    <section id="keahlian" class="section-shell pt-8">
      <div class="mb-10 flex flex-col justify-between gap-5 sm:flex-row sm:items-end"><div><p class="eyebrow">02 — Keahlian</p><h2 class="section-title">Teknologi yang saya gunakan.</h2></div><p class="max-w-md text-sm leading-6 text-slate-500">Perangkat kerja untuk membangun antarmuka, aplikasi server, dan produk web end-to-end.</p></div>
      <div class="grid grid-cols-2 gap-3 sm:grid-cols-3 lg:grid-cols-5 xl:grid-cols-9">
        <div v-for="skill in skills" :key="skill.name" class="skill-card" :class="[skill.border, `bg-gradient-to-br ${skill.tone}`]">
          <img v-if="skill.logo" :src="skill.logo" :alt="`Logo ${skill.name}`" class="h-11 w-11 object-contain" :class="{ invert: skill.invert, 'brightness-0 invert': skill.brighten }" loading="lazy" />
          <span v-else class="font-mono text-2xl font-black text-cyan-200">{{ skill.icon }}</span>
          <b>{{ skill.name }}</b>
        </div>
      </div>
    </section>

    <section id="pengalaman" class="section-shell">
      <div><p class="eyebrow">03 — Pengalaman</p><h2 class="section-title">Perjalanan profesional.</h2></div>
      <div class="relative mx-auto mt-14 max-w-4xl"><div class="timeline-line"></div><article v-for="(item, index) in experiences" :key="item.role + item.company" class="timeline-item"><div class="timeline-dot" :class="item.current ? 'current' : ''"><span>{{ String(index + 1).padStart(2, '0') }}</span></div><div class="glass-card group p-6 transition duration-300 hover:-translate-y-1 hover:border-cyan-300/25 sm:p-8"><div class="flex flex-col justify-between gap-3 sm:flex-row sm:items-start"><div><h3 class="font-display text-xl font-extrabold text-white sm:text-2xl">{{ item.role }}</h3><p class="mt-1 font-bold text-cyan-300">{{ item.company }}</p></div><span class="self-start rounded-full border border-white/10 bg-white/5 px-3 py-1.5 text-xs font-bold text-slate-400">{{ item.period }}</span></div><p class="mt-5 leading-7 text-slate-400">{{ item.description }}</p><p class="mt-4 text-xs font-semibold text-slate-600">⌖ {{ item.location }}</p></div></article></div>
    </section>

    <section class="section-shell pt-0"><div class="grid gap-5 lg:grid-cols-[1.2fr_.8fr]"><div class="glass-card relative overflow-hidden p-8"><p class="eyebrow">Pelatihan</p><h3 class="font-display text-2xl font-semibold text-white">Coding Camp powered by DBS Foundation</h3><p class="mt-2 text-sm font-semibold text-cyan-300">Front-End & Back-End Developer Cohort · 2025</p><p class="mt-5 max-w-2xl leading-7 text-slate-400">Program intensif yang memperkuat fundamental hingga advanced web development, Node.js, API, kolaborasi tim, dan integrasi Machine Learning dalam Capstone Project.</p></div><div class="glass-card p-8"><p class="eyebrow">Sertifikasi</p><ul class="divide-y divide-white/[.07]"><li v-for="cert in certifications" :key="cert" class="py-3 text-sm text-slate-300">{{ cert }}</li></ul></div></div></section>

    <section id="kontak" class="px-5 pb-10 pt-10 lg:px-8"><div class="contact-card mx-auto max-w-7xl overflow-hidden px-6 py-16 sm:px-12 sm:py-20"><p class="eyebrow">04 — Kontak</p><div class="grid gap-8 lg:grid-cols-[1fr_auto] lg:items-end"><div><h2 class="max-w-3xl font-display text-4xl font-semibold tracking-tight text-white sm:text-6xl">Mari bekerja bersama.</h2><p class="mt-5 max-w-xl leading-7 text-slate-400">Saya terbuka untuk diskusi mengenai proyek web, kolaborasi, dan peluang profesional.</p></div><div class="flex flex-wrap gap-4"><a href="mailto:faizbot81@gmail.com" class="primary-btn">Kirim email</a><a href="https://www.linkedin.com/in/faiz-akbar-putra-wardani" target="_blank" rel="noopener" class="secondary-btn">LinkedIn ↗</a></div></div></div><footer class="mx-auto flex max-w-7xl flex-col items-center justify-between gap-3 border-t border-white/10 py-8 text-xs text-slate-600 sm:flex-row"><span>© 2026 Faiz Akbar Putra Wardani.</span><span>Web Developer · Bandar Lampung</span></footer></section>
  </main>
</template>
