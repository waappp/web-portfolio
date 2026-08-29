<template>
  <main class="min-h-screen bg-background">

    <Navbar />

    <Hero />

    <ToolsSkills />

    <About />

    <Portfolio />

    <section
      id="contact"
      class="bg-section px-6 py-20 text-center sm:py-24 lg:px-8 lg:py-28"
    >
      <h2 class="text-3xl font-medium text-primary sm:text-4xl lg:text-5xl">
        Let’s build something great!
      </h2>
      <p class="mx-auto mt-5 max-w-md text-sm leading-6 text-secondary sm:text-base">
        Designing thoughtful interfaces.<br />
        Building meaningful digital experiences.
      </p>
      <a
        href="mailto:wafa@example.com"
        class="mt-8 inline-flex rounded-md bg-accent px-6 py-3 text-sm font-medium text-white transition hover:bg-accent-light"
      >
        Let's Talk
      </a>
    </section>

    <Footer />

  </main>
</template>