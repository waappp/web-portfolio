<script setup lang="ts">
import { ref, computed } from 'vue'

type Category = 'All' | 'UI Design' | 'Website'

interface Project {
  title: string
  category: Exclude<Category, 'All'>
  description: string
  image: string
  slug: string
  tools: string[]
}

const activeCategory = ref<Category>('All')

const projects: Project[] = [
  {
    title: 'CeptionCare',
    category: 'UI Design',
    description:
      'Healthcare digital experience designed with a clean and intuitive interface.',
    image: '/images/portfolio/medic.png',
    slug: 'ceptioncare',
    tools: ['Figma', 'UI/UX'],
  },

  {
    title: 'Tacklex',
    category: 'UI Design',
    description:
      'Modern rugby website concept with a bold visual identity and engaging experience.',
    image: '/images/portfolio/sport.png',
    slug: 'tacklex',
    tools: ['Figma', 'UI/UX'],
  },

  {
    title: 'SparkVibe',
    category: 'UI Design',
    description:
      'Creative agency website concept focused on visual storytelling and usability.',
    image: '/images/portfolio/agency.png',
    slug: 'sparkvibe',
    tools: ['Figma', 'UI/UX'],
  },

  {
    title: 'Furnistore',
    category: 'UI Design',
    description:
      'Modern furniture e-commerce website with a clean and responsive interface.',
    image: '/images/portfolio/furnistore.png',
    slug: 'furnistore',
    tools: ['Figma', 'UI/UX'],
  },

  {
    title: 'Omahmu Residence',
    category: 'UI Design',
    description:
      'A modern real estate website designed to simplify property discovery and create a seamless browsing experience.',
    image: '/images/portfolio/estate.png',
    slug: 'omahmu',
    tools: ['Figma', 'UI/UX'],
  },

  {
    title: 'Hype Kicks',
    category: 'UI Design',
    description:
      'A bold e-commerce experience built for sneaker enthusiasts and modern streetwear culture.',
    image: '/images/portfolio/shoes.png',
    slug: 'hypekicks',
    tools: ['Figma', 'UI/UX'],
  },

  {
    title: 'Furnistore Website',
    category: 'Website',
    description:
      'Modern furniture e-commerce website with a clean and responsive interface.',
    image: '/images/portfolio/furnistore.png',
    slug: 'furnistoreweb',
    tools: ['Nuxt', 'Tailwind CSS'],
  },
  {
    title: 'HypeKicks Website',
    category: 'Website',
    description:
      'A warm, product-led storefront for browsing footwear with ease.',
    image: '/images/portfolio/hypekicks.png',
    slug: 'hypekicksweb',
    tools: ['Nuxt', 'Tailwind CSS'],
  }
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
  <main class="min-h-screen bg-background">

    <Navbar />

    <!-- ========================= -->
    <!-- PORTFOLIO HERO -->
    <!-- ========================= -->

    <section class="px-6 pb-16 pt-36 lg:px-8">
      <div class="mx-auto max-w-7xl">

        <p
          class="text-sm font-medium uppercase tracking-[0.25em] text-accent"
        >
          My Work
        </p>

        <h1
          class="mt-4 max-w-3xl text-4xl font-semibold tracking-tight text-primary sm:text-5xl lg:text-6xl"
        >
          Creative Portfolio
        </h1>

        <p
          class="mt-6 max-w-2xl text-sm leading-7 text-secondary sm:text-base"
        >
          A collection of selected UI/UX designs and websites
          I've designed and developed.
        </p>

      </div>
    </section>


    <!-- ========================= -->
    <!-- FILTER -->
    <!-- ========================= -->

    <section class="px-6 pb-8 lg:px-8">
      <div class="mx-auto flex max-w-7xl flex-wrap gap-3">

        <button
          v-for="category in ['All', 'UI Design', 'Website']"
          :key="category"
          type="button"
          @click="activeCategory = category as Category"
          :class="
            activeCategory === category
              ? 'bg-accent text-white'
              : 'border border-primary/20 text-primary hover:border-accent hover:text-accent'
          "
          class="rounded-full px-6 py-2.5 text-sm font-medium transition-all duration-300"
        >
          {{ category }}
        </button>

      </div>
    </section>


    <!-- ========================= -->
    <!-- PROJECTS -->
    <!-- ========================= -->

    <section class="px-6 pb-24 lg:px-8">
      <div
        class="mx-auto grid max-w-7xl gap-7 md:grid-cols-2 lg:grid-cols-3"
      >

        <article
          v-for="project in filteredProjects"
          :key="project.slug"
          class="group overflow-hidden rounded-2xl border border-white/5 bg-card transition-all duration-500 hover:-translate-y-2 hover:border-accent/30"
        >

          <!-- Image -->

          <NuxtLink
            :to="`/projects/${project.slug}`"
            class="block overflow-hidden"
          >
            <div class="aspect-[16/10] overflow-hidden">

              <img
                :src="project.image"
                :alt="project.title"
                class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-105"
              />

            </div>
          </NuxtLink>


          <!-- Content -->

          <div class="p-6">

            <div class="flex items-start justify-between gap-4">

              <div>
                <p
                  class="text-xs font-medium uppercase tracking-wider text-accent"
                >
                  {{ project.category }}
                </p>

                <h2
                  class="mt-2 text-xl font-semibold text-primary"
                >
                  {{ project.title }}
                </h2>
              </div>

            </div>


            <p
              class="mt-4 text-sm leading-6 text-secondary"
            >
              {{ project.description }}
            </p>


            <!-- Tools -->

            <div class="mt-5 flex flex-wrap gap-2">

              <span
                v-for="tool in project.tools"
                :key="tool"
                class="rounded-full bg-white/5 px-3 py-1 text-xs text-secondary"
              >
                {{ tool }}
              </span>

            </div>


            <!-- Link -->

            <NuxtLink
              :to="`/projects/${project.slug}`"
              class="mt-6 inline-flex items-center gap-2 text-sm font-medium text-primary transition-colors hover:text-accent"
            >
              View Case Study

              <span
                class="transition-transform duration-300 group-hover:translate-x-1"
              >
                →
              </span>
            </NuxtLink>

          </div>

        </article>

      </div>
    </section>


    <Footer />

  </main>
</template>