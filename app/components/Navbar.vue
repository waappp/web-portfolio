<script setup lang="ts">
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <header class="fixed top-0 left-0 z-50 w-full border-b border-white/5 bg-background/95 backdrop-blur-md">
    <nav class="mx-auto flex max-w-7xl items-center justify-between px-6 py-5 lg:px-8">
      <!-- Logo -->
      <NuxtLink
        to="/"
        class="text-lg font-semibold text-primary"
        @click="closeMenu"
      >
        Hukama Niamul Wafa
      </NuxtLink>

      <!-- Desktop Navigation -->
      <div class="hidden items-center gap-10 md:flex">
        <NuxtLink
          to="/"
          class="text-sm text-secondary transition hover:text-accent"
        >
          Home
        </NuxtLink>

        <a
          href="#about"
          class="text-sm text-secondary transition hover:text-accent"
        >
          About
        </a>

        <a
          href="#portfolio"
          class="text-sm text-secondary transition hover:text-accent"
        >
          Portfolio
        </a>

        <a
          href="#contact"
          class="text-sm text-secondary transition hover:text-accent"
        >
          Contact
        </a>
      </div>

      <!-- Mobile Menu Button -->
      <button
        type="button"
        class="inline-flex items-center justify-center rounded-md border border-white/10 p-2 text-secondary md:hidden"
        aria-label="Toggle menu"
        @click="toggleMenu"
      >
        <span class="sr-only">Open menu</span>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="1.8"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>

      <!-- Let's Talk -->
      <a
        href="#contact"
        class="hidden rounded-md border border-accent px-5 py-2 text-sm text-primary transition hover:bg-accent md:block"
      >
        Let's Talk
      </a>
    </nav>

    <!-- Mobile Navigation -->
    <div v-if="isMenuOpen" class="border-t border-white/5 bg-background/95 px-6 py-4 md:hidden">
      <div class="flex flex-col gap-3">
        <NuxtLink
          to="/"
          class="text-sm text-secondary transition hover:text-accent"
          @click="closeMenu"
        >
          Home
        </NuxtLink>

        <a
          href="#about"
          class="text-sm text-secondary transition hover:text-accent"
          @click="closeMenu"
        >
          About
        </a>

        <a
          href="#portfolio"
          class="text-sm text-secondary transition hover:text-accent"
          @click="closeMenu"
        >
          Portfolio
        </a>

        <a
          href="#contact"
          class="text-sm text-secondary transition hover:text-accent"
          @click="closeMenu"
        >
          Contact
        </a>
      </div>
    </div>
  </header>
</template>