<template>
  <section
    id="home"
    class="relative min-h-[calc(100vh-80px)] overflow-hidden pt-20 lg:pt-16"
  >
    <div
      class="mx-auto grid min-h-[calc(100vh-80px)] w-full max-w-7xl items-center gap-8 px-6 lg:grid-cols-2 lg:px-8"
    >

      <div class="relative z-10 max-w-2xl">

        <p
          class="mb-3 text-2xl font-light text-primary sm:text-3xl"
        >
          Hello there!
        </p>

        <h1
          class="text-4xl font-semibold leading-[1.1] tracking-tight text-primary sm:text-5xl lg:text-10xl"
        >
          I am
          <span class="text-accent">
            Hukama Niamul Wafa
          </span>
        </h1>

        <p
          class="mt-5 text-base font-medium text-primary sm:text-lg"
        >
          UI/UX Designer & Frontend Developer
        </p>

        <p
          class="mt-5 max-w-xl text-sm leading-relaxed text-secondary sm:text-base"
        >
          I design thoughtful interfaces and bring them to life
          through clean, responsive, and engaging frontend
          development.
        </p>

        <div class="mt-7 flex flex-wrap gap-4">

          <a
            href="/CV.pdf"
            download="CV.pdf"
            class="rounded-md bg-accent px-6 py-3 text-sm font-medium text-white transition-all duration-300 hover:-translate-y-1 hover:bg-accent-light"
          >
            Download CV
          </a>

          <a
            href="#portfolio"
            class="rounded-md border border-primary/70 px-6 py-3 text-sm font-medium text-primary transition-all duration-300 hover:-translate-y-1 hover:border-accent hover:text-accent"
          >
            View My Work
          </a>

        </div>
      </div>

      <div
        class="relative flex h-[430px] items-center justify-center sm:h-[500px] lg:h-[560px]"
      >

        <div
          class="absolute right-[8%] top-[5%] h-16 w-16 rounded-full bg-accent/10 sm:h-20 sm:w-20 lg:h-24 lg:w-24"
        ></div>


        <div
          class="relative flex h-full w-full items-center justify-center"
        >

          <div
            class="absolute left-1/2 top-1/2 h-[280px] w-[340px] -translate-x-1/2 -translate-y-1/2 rotate-12 skew-y-3 rounded-[63%_37%_52%_48%_/_42%_58%_38%_62%] bg-gradient-to-br from-accent-light to-accent sm:h-[340px] sm:w-[420px] lg:h-[390px] lg:w-[500px]"
          ></div>

          <img
            src="/images/profile/wafa.png"
            alt="Hukama Niamul Wafa"
            class="relative z-10 -translate-y-7 h-[330px] w-auto object-contain [clip-path:polygon(0_0,100%_0,100%_96%,85%_98%,50%_100%,15%_98%,0_96%)] sm:-translate-y-8 sm:h-[400px] lg:-translate-y-9 lg:h-[460px]"
          />

        </div>

      </div>

    </div>

    <a
      href="mailto:hukamanw@gmail.com?subject=Let's%20Work%20Together"
      aria-label="Send email"
      title="Send email"
      class="fixed bottom-6 right-6 z-40 flex h-14 w-14 items-center justify-center rounded-full bg-accent text-white shadow-lg shadow-accent/25 transition-all duration-300 hover:-translate-y-1 hover:bg-accent-light hover:shadow-xl hover:shadow-accent/30 focus:outline-none focus:ring-2 focus:ring-accent focus:ring-offset-2 focus:ring-offset-background"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="1.8"
        class="h-6 w-6"
        aria-hidden="true"
      >
        <rect x="3" y="5" width="18" height="14" rx="2" />
        <path d="m3 7 9 6 9-6" />
      </svg>
    </a>
  </section>
</template>