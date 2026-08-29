<template>
  <section
    id="home"
    class="relative min-h-[calc(100vh-80px)] overflow-hidden pt-20 lg:pt-16"
  >
    <div
      class="mx-auto grid min-h-[calc(100vh-80px)] w-full max-w-7xl items-center gap-8 px-6 lg:grid-cols-2 lg:px-8"
    >

      <!-- ========================= -->
      <!-- LEFT CONTENT -->
      <!-- ========================= -->
      <div class="relative z-10 max-w-2xl">

        <!-- Greeting -->
        <p
          class="mb-3 text-2xl font-light text-primary sm:text-3xl"
        >
          Hello there!
        </p>

        <!-- Heading -->
        <h1
          class="text-4xl font-semibold leading-[1.1] tracking-tight text-primary sm:text-5xl lg:text-10xl"
        >
          I am
          <span class="text-accent">
            Hukama Niamul Wafa
          </span>
        </h1>

        <!-- Role -->
        <p
          class="mt-5 text-base font-medium text-primary sm:text-lg"
        >
          UI/UX Designer & Frontend Developer
        </p>

        <!-- Description -->
        <p
          class="mt-5 max-w-xl text-sm leading-relaxed text-secondary sm:text-base"
        >
          I design thoughtful interfaces and bring them to life
          through clean, responsive, and engaging frontend
          development.
        </p>

        <!-- Buttons -->
        <div class="mt-7 flex flex-wrap gap-4">

          <!-- Download CV -->
          <a
            href="/cv.pdf"
            download
            class="rounded-md bg-accent px-6 py-3 text-sm font-medium text-white transition-all duration-300 hover:-translate-y-1 hover:bg-accent-light"
          >
            Download CV
          </a>

          <!-- More -->
          <a
            href="#about"
            class="rounded-md border border-primary/70 px-6 py-3 text-sm font-medium text-primary transition-all duration-300 hover:-translate-y-1 hover:border-accent hover:text-accent"
          >
            More
          </a>

        </div>
      </div>


      <!-- ========================= -->
      <!-- RIGHT VISUAL -->
      <!-- ========================= -->
      <div
        class="relative flex h-[430px] items-center justify-center sm:h-[500px] lg:h-[560px]"
      >

        <!-- Decorative Circle -->
        <div
          class="absolute right-[8%] top-[5%] h-16 w-16 rounded-full bg-accent/10 sm:h-20 sm:w-20 lg:h-24 lg:w-24"
        ></div>


        <!-- VISUAL GROUP -->
        <div
          class="relative flex h-full w-full items-center justify-center"
        >

          <!-- Green Abstract Background -->
          <div
            class="absolute left-1/2 top-1/2 h-[280px] w-[340px] -translate-x-1/2 -translate-y-1/2 rotate-12 skew-y-3 rounded-[63%_37%_52%_48%_/_42%_58%_38%_62%] bg-gradient-to-br from-accent-light to-accent sm:h-[340px] sm:w-[420px] lg:h-[390px] lg:w-[500px]"
          ></div>

          <!-- Profile Image -->
          <img
            src="/images/profile/wafa.png"
            alt="Hukama Niamul Wafa"
            class="relative z-10 -translate-y-7 h-[360px] w-auto object-contain sm:-translate-y-8 sm:h-[440px] lg:-translate-y-9 lg:h-[500px]"
          />

        </div>

      </div>

    </div>
  </section>
</template>