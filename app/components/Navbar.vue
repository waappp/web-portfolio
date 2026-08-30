<template>
  <header class="fixed top-0 left-0 z-50 w-full border-b border-white/5 bg-background/95 backdrop-blur-md">
    <nav
      class="mx-auto flex max-w-7xl items-center justify-between px-6 py-5 lg:px-8"
    >
      <!-- Logo -->
      <NuxtLink
        to="/"
        class="text-lg font-semibold text-primary"
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

      <!-- Let's Talk -->
      <a
        href="mailto:hukamanw@gmail.com?subject=Let's%20Work%20Together"
        class="hidden rounded-md border border-accent px-5 py-2 text-sm text-primary transition hover:bg-accent md:block"
      >
        Let's Talk
      </a>
    </nav>
  </header>
</template>