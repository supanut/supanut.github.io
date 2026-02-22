<script setup lang="ts">
import { useSeoMeta } from '#imports'

useSeoMeta({
  title: 'Supanut Vatesaranasutee - Chief Technology Product Officer',
  description: 'Chief Technology Product Officer with 9+ years of experience in software engineering and technology leadership. Specializing in system architecture, mobile/web development, and digital health.',
  ogTitle: 'Supanut Vatesaranasutee | CTPO',
  ogDescription: 'Portfolio of Supanut Vatesaranasutee, Technology Leader & CTPO at Evolt Technology.',
})

const experience = [
  {
    role: 'Chief Technology Product Officer',
    company: 'Evolt Technology',
    period: 'Present',
    description: 'Leading technology and product strategy, overseeing engineering teams, and driving innovation in EV charging solutions.',
    icon: 'i-heroicons-bolt',
  },
  {
    role: 'Senior Solutions Architect',
    company: 'KASIKORN Business-Technology Group (KBTG)',
    period: 'Previous',
    description: 'Designed scalable system architectures and led technical initiatives for enterprise-grade financial applications.',
    icon: 'i-heroicons-building-library',
  },
  {
    role: 'Head of Technology for Digital Health',
    company: 'True Digital Group',
    period: 'Previous',
    description: 'Built and mentored a 20-member technology team. Developed digital health products driving significant user growth and strategic partnerships.',
    icon: 'i-heroicons-heart',
  },
  {
    role: 'System Engineer',
    company: 'Netservice Co., Ltd.',
    period: 'Previous',
    description: 'Started career focusing on system engineering, infrastructure, and core software solutions.',
    icon: 'i-heroicons-server',
  }
]

const skills = [
  { name: 'System Architecture', icon: 'i-heroicons-rectangle-group' },
  { name: 'Technology Leadership', icon: 'i-heroicons-users' },
  { name: 'Product Strategy', icon: 'i-heroicons-chart-bar' },
  { name: 'Mobile App Development', icon: 'i-heroicons-device-phone-mobile' },
  { name: 'Web Development', icon: 'i-heroicons-computer-desktop' },
  { name: 'Team Mentoring', icon: 'i-heroicons-academic-cap' },
  { name: 'Digital Health', icon: 'i-heroicons-heart' },
  { name: 'EV Technology', icon: 'i-heroicons-bolt' },
]

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
            Chief Technology Product Officer seamlessly blending <span
              class="font-semibold text-neutral-900 dark:text-neutral-100">engineering depth</span> with <span
              class="font-semibold text-neutral-900 dark:text-neutral-100">product vision</span>.
          </p>
        </div>

        <div class="flex flex-wrap items-center gap-4 pt-4">
          <UButton size="xl" color="primary" to="https://www.linkedin.com/in/supanut" target="_blank"
            trailing-icon="i-heroicons-arrow-up-right" class="font-semibold px-6 shadow-md shadow-primary-500/20">
            Let's Connect
          </UButton>
          <UButton size="xl" color="neutral" variant="soft" to="mailto:supanut@example.com"
            trailing-icon="i-heroicons-envelope" class="font-semibold px-6">
            Get in touch
          </UButton>
        </div>
      </section>

      <!-- Experience -->
      <section class="space-y-10 animate-fade-in-up" style="animation-delay: 100ms;">
        <div class="space-y-2">
          <h2 class="text-3xl font-bold tracking-tight flex items-center gap-2">
            <UIcon name="i-heroicons-briefcase" class="text-primary-500 w-8 h-8" />
            Professional Experience
          </h2>
          <p class="text-neutral-500 dark:text-neutral-400 text-lg">My 9+ years journey in tech leadership and
            architecture.</p>
        </div>

        <div class="space-y-6">
          <UCard v-for="job in experience" :key="job.company"
            class="group transition-all duration-300 hover:ring-2 hover:ring-primary-500/50 dark:hover:ring-primary-400/50 hover:shadow-lg dark:hover:shadow-primary-900/10">
            <template #header>
              <div class="flex flex-col md:flex-row md:items-start justify-between gap-4">
                <div class="flex items-center gap-4">
                  <div
                    class="p-3 rounded-lg bg-neutral-100 dark:bg-neutral-800 text-neutral-700 dark:text-neutral-300 group-hover:bg-primary-50 dark:group-hover:bg-primary-950/50 group-hover:text-primary-500 dark:group-hover:text-primary-400 transition-colors">
                    <UIcon :name="job.icon" class="w-6 h-6" />
                  </div>
                  <div>
                    <h3 class="text-xl font-bold text-neutral-900 dark:text-white">{{ job.role }}</h3>
                    <p class="text-md font-medium text-primary-600 dark:text-primary-400">{{ job.company }}</p>
                  </div>
                </div>
                <UBadge color="neutral" variant="soft" size="md" class="w-fit self-start md:self-auto">{{ job.period }}
                </UBadge>
              </div>
            </template>
            <p class="text-neutral-600 dark:text-neutral-400 text-lg leading-relaxed">
              {{ job.description }}
            </p>
          </UCard>
        </div>
      </section>

      <div class="grid md:grid-cols-5 gap-10 animate-fade-in-up" style="animation-delay: 200ms;">

        <!-- Skills -->
        <section class="md:col-span-3 space-y-8">
          <h2 class="text-3xl font-bold tracking-tight flex items-center gap-2">
            <UIcon name="i-heroicons-wrench-screwdriver" class="text-primary-500 w-8 h-8" />
            Core Expertise
          </h2>
          <div class="flex flex-wrap gap-3">
            <UBadge v-for="skill in skills" :key="skill.name" color="neutral" variant="soft" size="lg"
              class="px-4 py-2 text-sm font-medium hover:bg-neutral-200 dark:hover:bg-neutral-800 transition-colors">
              <UIcon :name="skill.icon" class="mr-2 w-4 h-4 opacity-70" />
              {{ skill.name }}
            </UBadge>
          </div>
        </section>

        <!-- Education -->
        <section class="md:col-span-2 space-y-8">
          <h2 class="text-3xl font-bold tracking-tight flex items-center gap-2">
            <UIcon name="i-heroicons-academic-cap" class="text-primary-500 w-8 h-8" />
            Education
          </h2>
          <UCard
            class="bg-gradient-to-br from-neutral-100 to-neutral-50 dark:from-neutral-900 dark:to-neutral-950 shadow-sm transition-transform hover:-translate-y-1">
            <div class="space-y-3">
              <div
                class="inline-flex items-center justify-center p-2 rounded-lg bg-blue-100 dark:bg-blue-900/30 text-blue-600 dark:text-blue-400 m-0">
                <UIcon name="i-heroicons-building-library" class="w-6 h-6" />
              </div>
              <div>
                <h3 class="text-xl font-bold text-neutral-900 dark:text-white leading-tight">Chulalongkorn University
                </h3>
                <p class="text-neutral-600 dark:text-neutral-400 font-medium">Bachelor of Engineering</p>
                <p class="text-sm text-neutral-500 dark:text-neutral-500">Computer Engineering</p>
              </div>
            </div>
          </UCard>
        </section>

      </div>

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