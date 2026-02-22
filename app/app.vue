<script setup lang="ts">
import { useSeoMeta } from '#imports'

useSeoMeta({
  title: 'Supanut Vatesaranasutee - Senior Solution Architect & Technology Leader',
  description: 'Technical leader and Full-Stack Software Engineer with 15+ years of experience. Specializing in system architecture, mobile/web development, and digital health.',
  ogTitle: 'Supanut Vatesaranasutee | Tech Leader',
  ogDescription: 'Portfolio of Supanut Vatesaranasutee, Senior Solution Architect at IBM Digital Talent for Business.',
})

const getLogoUrl = (domain: string) => `https://t3.gstatic.com/faviconV2?client=SOCIAL&type=FAVICON&fallback_opts=TYPE,SIZE,URL&url=https://${domain}&size=128`



const links = [
  { label: 'LinkedIn', icon: 'i-simple-icons-linkedin', to: 'https://www.linkedin.com/in/supanut' },
  { label: 'GitHub', icon: 'i-simple-icons-github', to: 'https://github.com/supanut' }
]
</script>

<template>
  <div
    class="min-h-screen bg-neutral-50 dark:bg-neutral-950 font-sans text-neutral-900 dark:text-neutral-100 selection:bg-primary-500/30">
    <UContainer class="max-w-4xl py-12 md:py-24 space-y-24">

      <!-- Header / Nav -->
      <header class="flex items-center justify-between">
        <div
          class="font-bold text-2xl tracking-tight bg-clip-text text-transparent bg-gradient-to-r from-primary-500 to-primary-700 dark:from-primary-400 dark:to-primary-600">
          SV.
        </div>
        <div class="flex items-center gap-2">
          <UButton v-for="link in links" :key="link.label" :icon="link.icon" :to="link.to" target="_blank"
            color="neutral" variant="ghost" size="sm" />
        </div>
      </header>

      <!-- Hero Section -->
      <section class="space-y-8 animate-fade-in-up">
        <div class="space-y-4">
          <UBadge color="primary" variant="subtle" size="md" class="rounded-full rounded-tl-none px-3 font-medium">
            <UIcon name="i-heroicons-hand-raised" class="mr-1 w-4 h-4" /> Hello, World
          </UBadge>

          <h1 class="text-5xl md:text-7xl font-extrabold tracking-tight text-balance leading-tight">
            I'm Supanut <br />
            <span class="text-primary-500 dark:text-primary-400">Vatesaranasutee</span>
          </h1>

          <p class="text-xl md:text-2xl text-neutral-600 dark:text-neutral-400 max-w-2xl text-balance leading-relaxed">
            Technical leader and Full-Stack Software Engineer with <span
              class="font-semibold text-neutral-900 dark:text-neutral-100">15+ years of experience</span>.
          </p>
        </div>

        <div class="flex flex-wrap items-center gap-4 pt-4">
          <UButton size="xl" color="primary" to="https://www.linkedin.com/in/supanut" target="_blank"
            trailing-icon="i-heroicons-arrow-up-right" class="font-semibold px-6 shadow-md shadow-primary-500/20">
            Let's Connect
          </UButton>
          <UButton size="xl" color="neutral" variant="soft" to="mailto:supanut.vt@gmail.com"
            trailing-icon="i-heroicons-envelope" class="font-semibold px-6">
            Get in touch
          </UButton>
        </div>
      </section>


      <!-- Footer -->
      <UFooter
        class="pt-12 pb-6 flex flex-col items-center gap-4 text-neutral-500 dark:text-neutral-400 animate-fade-in-up"
        style="animation-delay: 300ms;">
        <div class="w-full flex flex-col md:flex-row items-center justify-between gap-4">
          <p class="font-medium text-sm">
            © {{ new Date().getFullYear() }} Supanut Vatesaranasutee.
          </p>
          <div
            class="flex items-center gap-1 text-sm bg-neutral-100 dark:bg-neutral-800 px-3 py-1.5 rounded-full border border-neutral-200 dark:border-neutral-700">
            Built with
            <UIcon name="i-simple-icons-nuxtdotjs" class="text-green-500 w-4 h-4 mx-1" /> Nuxt &
            <UIcon name="i-simple-icons-tailwindcss" class="text-sky-400 w-4 h-4 ml-1" /> Tailwind CSS
          </div>
        </div>
      </UFooter>

    </UContainer>
  </div>
</template>

<style>
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  opacity: 0;
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}
</style>