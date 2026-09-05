<script setup lang="ts">
const menuOpen = ref(false)
</script>

<template>
  <header class="fixed top-0 left-0 z-50 w-full border-b border-white/5 bg-background/95 backdrop-blur-md">
    <nav
      class="mx-auto flex max-w-7xl items-center justify-between px-6 py-5 lg:px-8"
    >
      <NuxtLink
        to="/"
        class="flex items-center gap-3 text-lg font-semibold text-primary"
      >
        <img
          src="/wapa.png"
          alt="Wafa logo"
          class="h-8 w-8 object-contain sm:h-9 sm:w-9"
        />
        Hukama Niamul Wafa
      </NuxtLink>

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

      <a
        href="mailto:hukamanw@gmail.com?subject=Let's%20Work%20Together"
        class="hidden rounded-md border border-accent px-5 py-2 text-sm text-primary transition hover:bg-accent md:block"
      >
        Let's Talk
      </a>

      <button
        type="button"
        :aria-expanded="menuOpen"
        aria-label="Toggle navigation menu"
        class="flex h-10 w-10 items-center justify-center rounded-md text-primary transition hover:bg-accent/10 md:hidden"
        @click="menuOpen = !menuOpen"
      >
        <svg
          v-if="!menuOpen"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          class="h-6 w-6"
          aria-hidden="true"
        >
          <path d="M4 6h16M4 12h16M4 18h16" />
        </svg>

        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          class="h-6 w-6"
          aria-hidden="true"
        >
          <path d="M6 6l12 12M18 6 6 18" />
        </svg>
      </button>
    </nav>

    <div
      v-if="menuOpen"
      class="border-t border-white/5 bg-background px-6 py-4 md:hidden"
    >
      <div class="flex flex-col gap-4">
        <NuxtLink
          to="/"
          class="text-sm text-secondary transition hover:text-accent"
          @click="menuOpen = false"
        >
          Home
        </NuxtLink>

        <a
          href="#about"
          class="text-sm text-secondary transition hover:text-accent"
          @click="menuOpen = false"
        >
          About
        </a>

        <a
          href="#portfolio"
          class="text-sm text-secondary transition hover:text-accent"
          @click="menuOpen = false"
        >
          Portfolio
        </a>

        <a
          href="#contact"
          class="text-sm text-secondary transition hover:text-accent"
          @click="menuOpen = false"
        >
          Contact
        </a>

        <a
          href="mailto:hukamanw@gmail.com?subject=Let's%20Work%20Together"
          class="w-fit rounded-md border border-accent px-5 py-2 text-sm text-primary transition hover:bg-accent"
          @click="menuOpen = false"
        >
          Let's Talk
        </a>
      </div>
    </div>
  </header>
</template>