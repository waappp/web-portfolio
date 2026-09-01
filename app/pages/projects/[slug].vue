<script setup lang="ts">
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

interface Project {
  title: string
  category: 'UI Design' | 'Website'
  subtitle: string
  description: string
  image: string
  year: string
  role: string
  tools: string[]
  problem: string
  solution: string
  process: string[]
  gallery: string[]
  liveUrl?: string
}

const projects: Record<string, Project> = {
  'ceptioncare': {
    title: 'CeptionCare',
    category: 'UI Design',
    subtitle: 'Healthcare experience designed around simplicity and usability.',
    description:
      'A healthcare digital experience focused on creating a clean, intuitive, and accessible interface for users.',
    image: '/images/portfolio/medic.png',
    year: '2025',
    role: 'UI/UX Designer',
    tools: ['Figma', 'UI/UX Design',],
    liveUrl: 'https://www.figma.com/design/JBsXiuc3m90OxTZPiepWwm/Magang-Wafa?node-id=175-42&t=ROCytZV7zQQ3KiVh-1',

    problem:
      'Healthcare applications can become difficult to navigate when users are presented with too much information and complex interactions.',

    solution:
      'I focused on simplifying the interface, creating clearer visual hierarchy, and designing a user flow that allows users to access important information with minimal effort.',

    process: [
      'Research & Understanding',
      'User Flow',
      'Wireframing',
      'UI Design',
      'Prototyping',
    ],

    gallery: [
      '/images/projects/ceptioncare/ceptioncare.png',
    ],
  },

  'sparkvibe': {
  title: 'SparkVibe',
  category: 'UI Design',
  subtitle: 'A modern digital experience for a creative agency.',
  description:
    'A creative agency website concept designed to showcase services, projects, and brand identity through a modern and engaging interface.',
  image: '/images/portfolio/agency.png',
  year: '2025',
  role: 'UI/UX Designer',
  tools: ['Figma', 'UI/UX Design', 'Prototyping'],
  liveUrl: 'https://www.figma.com/design/icb5745HGl0cq99KkQfXxz/Magang?node-id=404-67&t=tWYsNbFQwSitOlnR-1',

  problem:
    'Creative agencies need a digital presence that can communicate their visual identity while presenting their services and portfolio in a clear and engaging way.',

  solution:
    'I designed a modern and visually engaging interface with strong typography, clear content hierarchy, and structured sections to help visitors understand the agency and explore its work.',

  process: [
    'Research',
    'Moodboard',
    'Wireframing',
    'UI Design',
    'Prototyping',
  ],

  gallery: [
    '/images/projects/sparkvibe/sparkvibe.png',
  ],
},

  furnistore: {
    title: 'Furnistore',
    category: 'UI Design',
    subtitle: 'A modern furniture e-commerce experience.',
    description:
      'A responsive furniture e-commerce website designed with a clean visual system and intuitive shopping experience.',
    image: '/images/portfolio/furnistore.png',
    year: '2025',
    role: 'UI/UX Designer & Frontend Developer',
    tools: ['Figma', 'UI/UX Design', 'Prototyping'],
  	liveUrl: 'https://www.figma.com/design/icb5745HGl0cq99KkQfXxz/Magang?node-id=0-1&t=KyA3L1dQTZEHGKyf-1',

    problem:
      'Furniture e-commerce websites often contain large amounts of product information, making it important to maintain a clear browsing experience.',

    solution:
      'I created a structured interface with clear product hierarchy, simple navigation, and responsive layouts across different screen sizes.',

    process: [
      'Research',
      'Information Architecture',
      'Wireframing',
      'UI Design',
      'Frontend Development',
    ],

    gallery: [
      '/images/projects/furnistore/furnistore.png',
    ],
  },

  tacklex: {
    title: 'Tacklex',
    category: 'UI Design',
    subtitle: 'A bold digital experience for rugby.',
    description:
      'A modern rugby website concept designed to create a strong visual identity and engaging user experience.',
    image: '/images/portfolio/sport.png',
    year: '2025',
    role: 'UI/UX Designer',
    tools: ['Figma', 'UI/UX Design'],
    liveUrl: 'https://www.figma.com/design/JBsXiuc3m90OxTZPiepWwm/Magang-Wafa?node-id=352-2&t=ROCytZV7zQQ3KiVh-1',

    problem:
      'Sports websites need to communicate energy and information quickly while maintaining a strong visual identity.',

    solution:
      'I combined bold typography, strong imagery, and structured content sections to create a more dynamic sports experience.',

    process: [
      'Research',
      'Moodboard',
      'Wireframing',
      'UI Design',
      'Prototype',
    ],

    gallery: [
      '/images/projects/tacklex/tacklex.png',
    ],
  },

  omahmu: {
    title: 'Omahmu Residence',
    category: 'UI Design',
    subtitle: 'A modern real estate website designed to simplify property discovery and create a seamless browsing experience.',
    description:
      'A modern real estate website concept for Aruna Residence, designed to help users explore properties, discover available residences, and navigate the real estate experience through a clean and structured interface.',
    image: '/images/portfolio/estate.png',
    year: '2025',
    role: 'UI/UX Designer',
    tools: ['Figma', 'UI/UX Design'],
    liveUrl: 'https://www.figma.com/design/JBsXiuc3m90OxTZPiepWwm/Magang-Wafa?node-id=0-1&t=ROCytZV7zQQ3KiVh-1',

    problem:
      'Real estate websites often contain a large amount of property information, making it challenging for users to quickly discover properties that match their needs.',

    solution:
      'I designed a clean and structured experience with intuitive navigation, property-focused visuals, and a simple search interface to make property discovery easier and more engaging.',

    process: [
      'Research',
      'Moodboard',
      'Wireframing',
      'UI Design',
      'Prototype',
    ],

    gallery: [
      '/images/projects/omahmu/omahmu.png',
    ],
  },

  hypekicks: {
    title: 'Hype Kicks',
    category: 'UI Design',
    subtitle: 'A bold e-commerce experience for sneaker enthusiasts.',
    description:
      'A modern sneaker e-commerce website concept designed to showcase products through bold visuals, clear categorization, and an engaging shopping experience.',
    image: '/images/portfolio/shoes.png',
    year: '2025',
    role: 'UI/UX Designer',
    tools: ['Figma', 'UI/UX Design'],
	  liveUrl: 'https://www.figma.com/design/icb5745HGl0cq99KkQfXxz/Magang?node-id=217-67&t=flPgzi1GQEk2cMqz-1',

    problem:
      'Sneaker e-commerce platforms need to balance strong visual branding with an intuitive shopping experience, allowing users to discover products quickly without losing the excitement of the brand.',

    solution:
      'I created a bold and visually-driven interface with clear product categories, prominent imagery, and structured content to create an engaging experience for sneaker enthusiasts.',

    process: [
      'Research',
      'Moodboard',
      'Wireframing',
      'UI Design',
      'Prototype',
    ],

    gallery: [
      '/images/projects/hypekicks/hypekicks.png',
    ],
  },

  furnistoreweb: {
    title: 'Furnistore',
    category: 'Website',
    subtitle: 'A modern furniture e-commerce experience.',
    description:
      'A responsive furniture e-commerce website designed with a clean visual system and intuitive shopping experience.',
    image: '/images/portfolio/furnistore.png',
    year: '2025',
    role: 'UI/UX Designer & Frontend Developer',
    tools: ['VScode', 'Nuxt', 'Tailwind CSS'],
	 liveUrl: 'https://furnistore-sepia.vercel.app/',

    problem:
      'Furniture e-commerce websites often contain large amounts of product information, making it important to maintain a clear browsing experience.',

    solution:
      'I created a structured interface with clear product hierarchy, simple navigation, and responsive layouts across different screen sizes.',

    process: [
      'Research',
      'Information Architecture',
      'Wireframing',
      'UI Design',
      'Frontend Development',
    ],

    gallery: [
      '/images/projects/furnistore/furnistore.png',
    ],
  },
  hypekicksweb: {
    title: 'HypeKicks',
    category: 'Website',
    subtitle: 'A Bold E-Commerce Experience for Sneaker Enthusiasts',
    description:
      'HypeKicks is a modern sneaker e-commerce website concept designed to showcase sneakers through a bold visual identity and an engaging shopping experience. The interface combines strong typography, dynamic product imagery, and a structured layout to create a digital experience that feels energetic while remaining easy to navigate.',
    image: '/images/portfolio/hypekicks.png',
    year: '2025',
    role: 'UI/UX Designer & Frontend Developer',
    tools: ['VScode', 'Nuxt', 'Tailwind CSS'],
	  liveUrl: 'https://hype-kicks-lyart.vercel.app/',

    problem:
      'Sneaker websites need to do more than simply display products. They need to create a strong visual identity while making it easy for users to discover, compare, and explore products.',

    solution:
      'I created a bold and visually-driven interface that puts the products at the center of the experience. Clear navigation, structured product sections, strong typography, and carefully designed interactions help users explore the collection while maintaining the energetic character of HypeKicks.',

    process: [
      'Research',
      'Information Architecture',
      'Wireframing',
      'UI Design',
      'Frontend Development',
    ],

    gallery: [
      '/images/projects/hypekicks/hypekicks.png',
    ],
  },
}

const project = computed(() => {
  return projects[route.params.slug as string]
})

if (!project.value) {
  throw createError({
    statusCode: 404,
    statusMessage: 'Project Not Found',
  })
}
</script>


<template>
  <main
    v-if="project"
    class="min-h-screen bg-background"
  >

    <Navbar />

    <!-- ========================= -->
    <!-- PROJECT HERO -->
    <!-- ========================= -->

    <section
      class="px-6 pb-16 pt-36 lg:px-8 lg:pb-20"
    >
      <div class="mx-auto max-w-7xl">

        <!-- Back -->
        <NuxtLink
          to="/portfolio"
          class="group inline-flex items-center gap-2 text-sm text-secondary transition-colors hover:text-accent"
        >
          <span
            class="transition-transform duration-300 group-hover:-translate-x-1"
          >
            ←
          </span>

          Back to Portfolio
        </NuxtLink>


        <!-- Category -->

        <p
          class="mt-12 text-sm font-medium uppercase tracking-[0.25em] text-accent"
        >
          {{ project.category }}
        </p>


        <!-- Title -->

        <h1
          class="mt-4 max-w-4xl text-4xl font-semibold tracking-tight text-primary sm:text-5xl lg:text-7xl"
        >
          {{ project.title }}
        </h1>


        <!-- Subtitle -->

        <p
          class="mt-5 max-w-2xl text-base leading-7 text-secondary sm:text-lg"
        >
          {{ project.subtitle }}
        </p>


        <!-- Project Info -->

        <div
          class="mt-8 flex flex-wrap gap-x-10 gap-y-5"
        >

          <div>
            <p class="text-xs uppercase tracking-wider text-secondary">
              Year
            </p>

            <p class="mt-1 text-sm text-primary">
              {{ project.year }}
            </p>
          </div>


          <div>
            <p class="text-xs uppercase tracking-wider text-secondary">
              My Role
            </p>

            <p class="mt-1 text-sm text-primary">
              {{ project.role }}
            </p>
          </div>


          <div>
            <p class="text-xs uppercase tracking-wider text-secondary">
              Tools
            </p>

            <div class="mt-1 flex flex-wrap gap-2">

              <span
                v-for="tool in project.tools"
                :key="tool"
                class="text-sm text-primary"
              >
                {{ tool }}
              </span>

            </div>
          </div>

        </div>

		<div
  v-if="project.liveUrl"
  class="mt-8"
>
  <a
    :href="project.liveUrl"
    target="_blank"
    rel="noopener noreferrer"
    class="inline-flex items-center gap-2 rounded-lg bg-accent px-6 py-3 text-sm font-medium text-white transition-all duration-300 hover:-translate-y-1 hover:opacity-90"
  >
    View Live

    <span>↗</span>
  </a>
</div>

      </div>
    </section>


    <!-- ========================= -->
    <!-- COVER IMAGE -->
    <!-- ========================= -->

    <section class="px-6 lg:px-8">
      <div class="mx-auto max-w-7xl">

        <div
          class="overflow-hidden rounded-2xl border border-white/5 bg-card"
        >
          <img
            :src="project.image"
            :alt="project.title"
            class="h-auto w-full object-cover"
          />
        </div>

      </div>
    </section>


    <!-- ========================= -->
    <!-- OVERVIEW -->
    <!-- ========================= -->

    <section class="px-6 py-20 lg:px-8 lg:py-28">
      <div
        class="mx-auto grid max-w-5xl gap-12 lg:grid-cols-[0.7fr_1.3fr]"
      >

        <div>
          <p
            class="text-sm font-medium uppercase tracking-[0.25em] text-accent"
          >
            Overview
          </p>

          <h2
            class="mt-3 text-3xl font-semibold text-primary"
          >
            About the project
          </h2>
        </div>


        <div>
          <p
            class="text-base leading-8 text-secondary"
          >
            {{ project.description }}
          </p>
        </div>

      </div>
    </section>


    <!-- ========================= -->
    <!-- PROBLEM & SOLUTION -->
    <!-- ========================= -->

    <section class="bg-section px-6 py-20 lg:px-8 lg:py-28">
      <div
        class="mx-auto grid max-w-5xl gap-12 lg:grid-cols-2"
      >

        <!-- Problem -->

        <div>
          <p
            class="text-sm font-medium uppercase tracking-[0.25em] text-accent"
          >
            The Challenge
          </p>

          <h2
            class="mt-3 text-2xl font-semibold text-primary sm:text-3xl"
          >
            The Problem
          </h2>

          <p
            class="mt-5 text-sm leading-7 text-secondary sm:text-base"
          >
            {{ project.problem }}
          </p>
        </div>


        <!-- Solution -->

        <div>
          <p
            class="text-sm font-medium uppercase tracking-[0.25em] text-accent"
          >
            My Approach
          </p>

          <h2
            class="mt-3 text-2xl font-semibold text-primary sm:text-3xl"
          >
            The Solution
          </h2>

          <p
            class="mt-5 text-sm leading-7 text-secondary sm:text-base"
          >
            {{ project.solution }}
          </p>
        </div>

      </div>
    </section>


    <!-- ========================= -->
    <!-- DESIGN PROCESS -->
    <!-- ========================= -->

    <section class="px-6 py-20 lg:px-8 lg:py-28">
      <div class="mx-auto max-w-5xl">

        <div class="text-center">

          <p
            class="text-sm font-medium uppercase tracking-[0.25em] text-accent"
          >
            My Process
          </p>

          <h2
            class="mt-3 text-3xl font-semibold text-primary sm:text-4xl"
          >
            From idea to final product
          </h2>

        </div>


        <div
          class="mt-12 grid gap-4 sm:grid-cols-2 lg:grid-cols-5"
        >

          <div
            v-for="(step, index) in project.process"
            :key="step"
            class="rounded-2xl border border-white/5 bg-card p-6"
          >

            <span
              class="text-sm font-medium text-accent"
            >
              0{{ index + 1 }}
            </span>

            <p
              class="mt-4 text-sm font-medium text-primary"
            >
              {{ step }}
            </p>

          </div>

        </div>

      </div>
    </section>


    <!-- ========================= -->
    <!-- PROJECT GALLERY -->
    <!-- ========================= -->

    <section class="px-6 pb-20 lg:px-8 lg:pb-28">
      <div class="mx-auto max-w-7xl">

        <div class="mb-10">
          <p
            class="text-sm font-medium uppercase tracking-[0.25em] text-accent"
          >
            Visuals
          </p>

          <h2
            class="mt-3 text-3xl font-semibold text-primary sm:text-4xl"
          >
            Design Exploration
          </h2>
        </div>


        <div class="space-y-8">

          <div
            v-for="image in project.gallery"
            :key="image"
            class="overflow-hidden rounded-2xl border border-white/5 bg-card"
          >
            <img
              :src="image"
              :alt="project.title"
              class="h-auto w-full"
            />
          </div>

        </div>

      </div>
    </section>


    <!-- ========================= -->
    <!-- BACK TO PORTFOLIO -->
    <!-- ========================= -->

    <section class="px-6 pb-24 lg:px-8">
      <div class="mx-auto max-w-5xl text-center">

        <p class="text-sm text-secondary">
          Interested in seeing more?
        </p>

        <NuxtLink
          to="/portfolio"
          class="mt-4 inline-flex items-center gap-2 text-lg font-medium text-primary transition-colors hover:text-accent"
        >
          Explore more projects

          <span>
            →
          </span>
        </NuxtLink>

      </div>
    </section>


    <Footer />

  </main>
</template>