<script setup>
import { ref, computed } from 'vue'

const activeCategory = ref('UI Design')

const projects = [
  {
    title: 'CeptionCare',
    category: 'UI Design',
    description:
      'Healthcare interface focused on a clean and intuitive digital experience.',
    image: '/images/portfolio/medic.png',
    slug: 'ceptioncare',
  },
  {
    title: 'Tacklex',
    category: 'UI Design',
    description:
      'Modern rugby website concept with a bold visual identity and engaging layout.',
    image: '/images/portfolio/sport.png',
    slug: 'tacklex',
  },
  {
    title: 'SparkVibe',
    category: 'UI Design',
    description:
      'Creative agency website concept designed to showcase services and digital experiences.',
    image: '/images/portfolio/agency.png',
    slug: 'sparkvibe',
  },
  {
    title: 'Furnistore Website',
    category: 'Website',
    description:
      'A warm, product-led storefront for browsing furniture with ease.',
    image: '/images/portfolio/furnistore.png',
    slug: 'furnistoreweb',
  },
  {
   title: 'HypeKicks Website',
    category: 'Website',
    description:
      'A bold and modern sneaker e-commerce experience built for sneaker enthusiasts.',
    image: '/images/portfolio/shoes.png',
    slug: 'hypekicksweb',
  },
] 

const filteredProjects = computed(() => {
  if (activeCategory.value === 'All') {
    return projects
  }

  return projects.filter(
    (project) => project.category === activeCategory.value
  )
})
</script>

<template>
  <section
    id="portfolio"
    class="relative overflow-hidden py-20 sm:py-24 lg:py-28"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">

      <div class="max-w-3xl">

        <p
          class="text-sm font-medium uppercase tracking-[0.25em] text-accent"
        >
          Selected Works
        </p>

        <h2
          class="mt-3 text-3xl font-semibold tracking-tight text-primary sm:text-4xl lg:text-5xl"
        >
          My Creative Portfolio
        </h2>

        <p
          class="mt-4 max-w-2xl text-sm leading-7 text-secondary sm:text-base"
        >
          Explore a collection of my UI/UX designs and websites
          I've designed and developed, showcasing how I turn ideas
          into thoughtful and functional digital experiences.
        </p>

      </div>

      <div class="mt-8 flex flex-wrap gap-4">

        <button
          type="button"
          @click="activeCategory = 'UI Design'"
          :class="
            activeCategory === 'UI Design'
              ? 'bg-accent text-white'
              : 'border border-primary/40 text-primary hover:border-accent hover:text-accent'
          "
          class="rounded-full px-6 py-2.5 text-sm font-medium transition-all duration-300"
        >
          UI Design
        </button>

        <button
          type="button"
          @click="activeCategory = 'Website'"
          :class="
            activeCategory === 'Website'
              ? 'bg-accent text-white'
              : 'border border-primary/40 text-primary hover:border-accent hover:text-accent'
          "
          class="rounded-full px-6 py-2.5 text-sm font-medium transition-all duration-300"
        >
          Website
        </button>

      </div>


      <div
        class="mt-10 grid gap-6 md:grid-cols-2 lg:grid-cols-3"
      >

        <article
          v-for="project in filteredProjects"
          :key="project.slug"
          class="group overflow-hidden rounded-2xl border border-white/5 bg-card transition-all duration-300 hover:-translate-y-2 hover:border-accent/30"
        >

          <a
            v-if="project.url"
            :href="project.url"
            target="_blank"
            rel="noopener noreferrer"
            class="block overflow-hidden"
          >
            <div class="aspect-[16/10] overflow-hidden">

              <img
                :src="project.image"
                :alt="project.title"
                class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-105"
              />

            </div>
          </a>

          <NuxtLink
            v-else
            :to="`/projects/${project.slug}`"
            class="block overflow-hidden"
          >
            <div class="aspect-[16/10] overflow-hidden">
              <img
                :src="project.image"
                :alt="project.title"
                class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-105"
              />
            </div>
          </NuxtLink>

          <div class="p-5">

            <div class="flex items-center justify-between gap-3">

              <h3
                class="text-lg font-semibold text-primary"
              >
                {{ project.title }}
              </h3>

              <span
                class="text-xs font-medium text-accent"
              >
                {{ project.category }}
              </span>

            </div>

            <p
              class="mt-3 text-sm leading-6 text-secondary"
            >
              {{ project.description }}
            </p>

            <a
              v-if="project.url"
              :href="project.url"
              target="_blank"
              rel="noopener noreferrer"
              class="mt-5 inline-flex items-center gap-2 text-sm font-medium text-primary transition-colors hover:text-accent"
            >
              View Project

              <span
                class="transition-transform duration-300 group-hover:translate-x-1"
              >
                →
              </span>
            </a>

            <NuxtLink
              v-else
              :to="`/projects/${project.slug}`"
              class="mt-5 inline-flex items-center gap-2 text-sm font-medium text-primary transition-colors hover:text-accent"
            >
              View Project

              <span
                class="transition-transform duration-300 group-hover:translate-x-1"
              >
                →
              </span>
            </NuxtLink>

          </div>

        </article>

      </div>


      <div class="mt-10 flex justify-center">

        <NuxtLink
  to="/portfolio"
  class="rounded-md border border-primary/40 px-7 py-3 text-sm font-medium text-primary transition-all duration-300 hover:border-accent hover:text-accent"
>
  View All Projects
</NuxtLink>

      </div>

    </div>
  </section>
</template>