<template>
  <section
    id="about"
    class="relative overflow-hidden py-20 sm:py-24 lg:py-28"
  >
    <div
      class="mx-auto grid w-full max-w-7xl items-center gap-12 px-6 lg:grid-cols-[0.8fr_1.2fr] lg:gap-20 lg:px-8"
    >

      <!-- ========================= -->
      <!-- LEFT : PROFILE IMAGE -->
      <!-- ========================= -->
      <div
        class="relative flex min-h-[400px] items-center justify-center sm:min-h-[450px] lg:min-h-[500px]"
      >

        <!-- Decorative Circle -->
        <div
          class="absolute left-[10%] top-[8%] h-16 w-16 rounded-full bg-accent/10 sm:h-20 sm:w-20"
        ></div>

        <!-- Green Shape -->
        <div
          class="absolute left-1/2 top-1/2 h-[270px] w-[320px] -translate-x-1/2 -translate-y-1/2 -rotate-6 rounded-[55%_45%_48%_52%] bg-gradient-to-br from-accent-light to-accent sm:h-[330px] sm:w-[390px] lg:h-[360px] lg:w-[430px]"
        ></div>

        <!-- Profile -->
        <img
          src="/images/profile/wafa.png"
          alt="Hukama Niamul Wafa"
          class="relative z-10 h-[370px] w-auto object-contain sm:h-[430px] lg:h-[460px]"
        />

      </div>


      <!-- ========================= -->
      <!-- RIGHT : CONTENT -->
      <!-- ========================= -->
      <div>


        <!-- Title -->
        <h2
          class="mt-3 text-3xl font-semibold tracking-tight text-primary sm:text-4xl"
        >
          About Me
        </h2>

        <!-- Subtitle -->
        <p
          class="mt-2 text-base text-primary sm:text-lg"
        >
          Designing with purpose, building with code.
        </p>


        <!-- Paragraph 1 -->
        <p
          class="mt-7 text-sm leading-7 text-secondary sm:text-base"
        >
          Hi, I'm
          <span class="font-medium text-accent">
            Wafa
          </span>,
          a UI/UX Designer and Frontend Developer who enjoys
          turning ideas into meaningful digital experiences.
        </p>


        <!-- Paragraph 2 -->
        <p
          class="mt-5 text-sm leading-7 text-secondary sm:text-base"
        >
          I combine
          <span class="font-medium text-accent">
            design thinking
          </span>
          and
          <span class="font-medium text-accent">
            frontend development
          </span>
          to create interfaces that are not only visually
          engaging, but also intuitive, responsive, and functional.
          I enjoy the process of transforming ideas into
          wireframes and high-fidelity designs, then bringing
          them to life through interactive and responsive code.
        </p>


        <!-- Paragraph 3 -->
        <p
          class="mt-5 text-sm leading-7 text-secondary sm:text-base"
        >
          With a background in Information Technology, I'm
          continuously exploring the intersection between design,
          technology, and user experience. For me, a great digital
          product is where good design meets thoughtful development.
        </p>


        <!-- Closing -->
        <p
          class="mt-7 text-sm font-medium text-accent sm:text-base"
        >
          Design it. Build it. Make it work.
        </p>

      </div>

    </div>
  </section>
</template>