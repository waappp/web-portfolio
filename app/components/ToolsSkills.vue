<script setup lang="ts">
import { Icon } from '@iconify/vue'

const skills = [
  {
    name: 'Figma',
    icon: 'logos:figma',
  },
  {
    name: 'HTML',
    icon: 'logos:html-5',
  },
  {
    name: 'CSS',
    icon: 'logos:css-3',
  },
  {
    name: 'JavaScript',
    icon: 'logos:javascript',
  },
  {
    name: 'Vue',
    icon: 'logos:vue',
  },
  {
    name: 'Nuxt',
    icon: 'logos:nuxt-icon',
  },
  {
    name: 'Tailwind',
    icon: 'logos:tailwindcss-icon',
  },
  {
    name: 'Git',
    icon: 'logos:git-icon',
  },
]
</script>

<template>
  <section
    id="skills"
    class="relative py-20 sm:py-24 lg:py-28"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">

      <!-- Heading -->
      <div class="text-center">

        <h2
          class="mt-3 text-3xl font-semibold tracking-tight text-primary sm:text-4xl"
        >
          Tools & Skills
        </h2>

      </div>


      <!-- Skills -->
      <div
        class="mx-auto mt-12 grid max-w-5xl grid-cols-2 gap-5 sm:grid-cols-4 lg:grid-cols-8"
      >

        <div
          v-for="skill in skills"
          :key="skill.name"
          class="group flex aspect-square items-center justify-center rounded-xl border border-white/5 bg-card p-5 shadow-lg transition-all duration-300 hover:-translate-y-2 hover:border-accent/30 hover:bg-card/80"
        >

          <!-- Icon -->
          <Icon
            :icon="skill.icon"
            class="h-12 w-12 transition-transform duration-300 group-hover:scale-110 sm:h-16 sm:w-16"
          />

        </div>

      </div>

    </div>
  </section>
</template>