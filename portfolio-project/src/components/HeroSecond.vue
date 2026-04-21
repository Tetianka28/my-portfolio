<template>
  <section class="relative col-span-12 grid min-h-[500px] grid-cols-12 gap-x-4 gap-y-0 overflow-hidden py-16">
    <div class="background-hero"></div>
    <div class="relative z-10 col-start-2 col-span-10 h-fit self-start">
      <h1 class="text-2xl uppercase leading-none md:text-3xl font-[Perpetua] mb-2">
        Hi, I'M <span class="text-red-800 font-base font-[Perpetua] pl-2">Tetiana Tarasiuk</span>
      </h1>
    </div>

    <div class="relative z-10 col-start-2 col-span-10 grid gap-6 md:grid-cols-2 lg:grid-cols-[38%_62%]">
      <div class="flex min-h-[255px] items-center justify-center lg:justify-start">
        <img
          src="@/assets/img/picture-frame.png"
          alt="picture-frame"
          class="h-auto max-h-[255px] w-full max-w-[255px] object-contain"
        />
      </div>

      <div class="grid sm:grid-cols-2 sm:gap-8">
        <div>
          <h2 class="mb-6 text-sm font-medium uppercase font-[roboto] text-slate-800">
            Work Experience
          </h2>
          <div class="grid grid-cols-2 gap-4 text-sm font-[roboto] font-base text-slate-800">
            <div>
              <p class="uppercase ">Customer Service</p>
              <p class="text-sm text-slate-600">(1y+)</p>
            </div>
            <div>
              <p class="uppercase">Sales</p>
              <p class="text-sm text-slate-600">(3y)</p>
            </div>
            <div class="mt-2">
              <p class="uppercase">Operations</p>
              <p class="text-slate-600">(1y+)</p>
            </div>
          </div>

          <div class="mt-12">
            <div class="mb-4 flex gap-2 sm:mb-2">
               <svg xmlns="http://www.w3.org/2000/svg" width="38" height="38" viewBox="0 0 64 64"><path fill="#ffe62e" d="M32 62c16.6 0 30-13.4 30-30H2c0 16.6 13.4 30 30 30"/><path fill="#428bc1" d="M32 2C15.4 2 2 15.4 2 32h60C62 15.4 48.6 2 32 2"/></svg>
               <svg xmlns="http://www.w3.org/2000/svg" width="38" height="38" viewBox="0 0 64 64"><path fill="#f9f9f9" d="M32 2c16.6 0 30 13.4 30 30H2C2 15.4 15.4 2 32 2"/><path fill="#ed4c5c" d="M32 62C15.4 62 2 48.6 2 32h60c0 16.6-13.4 30-30 30"/></svg>
               <svg xmlns="http://www.w3.org/2000/svg" width="38" height="38" viewBox="0 0 64 64"><path fill="#2a5f9e" d="M22 60.3V46.5l-10.3 7.6c2.9 2.7 6.4 4.8 10.3 6.2m20 0c3.9-1.4 7.4-3.5 10.3-6.2L42 46.4zM3.7 42c.3 1 .7 1.9 1.2 2.9L8.8 42zm51.5 0l3.9 2.9c.4-.9.8-1.9 1.2-2.9z"/><path fill="#fff" d="M23.5 38H2.6c.3 1.4.7 2.7 1.1 4h5.1l-3.9 2.9c.8 1.7 1.7 3.2 2.8 4.7L18 42h4v2l-11.7 8.6l1.4 1.4L22 46.5v13.8c1.3.5 2.6.8 4 1.1V38zm37.9 0H38v23.4c1.4-.3 2.7-.7 4-1.1V46.5L52.3 54c1.4-1.3 2.6-2.7 3.8-4.2L45.4 42h6.8l6.1 4.5c.3-.5.6-1.1.8-1.6L55.2 42h5.1c.4-1.3.8-2.6 1.1-4"/><path fill="#ed4c5c" d="M7.7 49.6c.8 1.1 1.6 2.1 2.5 3.1L22 44.1v-2h-4zM45.5 42l10.7 7.8c.4-.5.7-1 1.1-1.5c.1-.1.1-.2.2-.2c.3-.5.7-1.1 1-1.6L52.2 42z"/><path fill="#2a5f9e" d="M42 3.7v13.8l10.3-7.6C49.4 7.2 45.9 5.1 42 3.7m-20 0c-3.9 1.4-7.4 3.5-10.3 6.2L22 17.6zM60.3 22c-.3-1-.7-1.9-1.2-2.9L55.2 22zM8.8 22l-3.9-2.9c-.4 1-.8 1.9-1.2 2.9z"/><path fill="#fff" d="M40.5 26h20.8c-.3-1.4-.7-2.7-1.1-4h-5.1l3.9-2.9c-.8-1.7-1.7-3.2-2.8-4.7L46 22h-4v-2l11.7-8.6l-1.4-1.4L42 17.5V3.7c-1.3-.5-2.6-.8-4-1.1V26zM2.6 26H26V2.6c-1.4.3-2.7.7-4 1.1v13.8L11.7 10c-1.4 1.3-2.6 2.7-3.8 4.2L18.6 22h-6.8l-6.1-4.5c-.3.5-.6 1.1-.8 1.6L8.8 22H3.7c-.4 1.3-.8 2.6-1.1 4"/><g fill="#ed4c5c"><path d="M56.3 14.4c-.8-1.1-1.6-2.1-2.5-3.1L42 19.9v2h4zM18.5 22L7.9 14.2c-.4.5-.7 1-1.1 1.5c-.1.1-.1.2-.2.2c-.3.5-.7 1.1-1 1.6l6.1 4.5z"/><path d="M61.4 26H38V2.6Q35.15 2 32 2c-3.15 0-4.1.2-6 .6V26H2.6Q2 28.85 2 32c0 3.15.2 4.1.6 6H26v23.4q2.85.6 6 .6c3.15 0 4.1-.2 6-.6V38h23.4q.6-2.85.6-6c0-3.15-.2-4.1-.6-6"/></g></svg>
               <svg xmlns="http://www.w3.org/2000/svg" width="38" height="38" viewBox="0 0 64 64"><path fill="#ed4c5c" d="M61.2 25C58 11.8 46.2 2 32 2h-1v23zM17 6C10 10.1 4.8 16.9 2.8 25H17zM2.8 39c2 8.1 7.2 14.9 14.2 19V39zM31 62h1c14.2 0 26-9.8 29.2-23H31z"/><path fill="#fff" d="M61.2 25H31V2c-5.1.2-9.9 1.6-14 4v19H2.8c-.5 2.2-.8 4.6-.8 7s.3 4.8.8 7H17v19c4.1 2.4 8.9 3.8 14 4V39h30.2c.5-2.2.8-4.6.8-7s-.3-4.8-.8-7"/></svg>
               <svg xmlns="http://www.w3.org/2000/svg" width="38" height="38" viewBox="0 0 64 64"><path fill="#f9f9f9" d="M31.9 2c-13 0-24.1 8.4-28.2 20h56.6C56.1 10.4 45 2 31.9 2"/><path fill="#ed4c5c" d="M31.9 62c13.1 0 24.2-8.4 28.3-20H3.7c4.1 11.7 15.2 20 28.2 20"/><path fill="#428bc1" d="M3.7 22C2.6 25.1 2 28.5 2 32s.6 6.9 1.7 10h56.6c1.1-3.1 1.7-6.5 1.7-10s-.6-6.9-1.7-10z"/></svg>

            </div>
          </div>
        </div>

        <div class="flex flex-col gap-8 font-[roboto]">
          <div>
            <h2 class="mb-6 text-sm font-medium uppercase font-[roboto] text-slate-800">
              Education
            </h2>
            <p class="text-sm font-base uppercase text-slate-800">Multimedia Design</p>
            <p class="text-xs text-slate-600 italic">Southern Denmark Business Academy</p>
            <p class="mt-1 text-xs text-slate-600">(2025 - present)</p>
          </div>

          <div>
            <p class="text-sm font-base uppercase text-slate-800">Japanese Language & Literature</p>
            <p class="text-xs text-slate-600 italic">Borys Grinchenko Kyiv Metropolitan University</p>
            <p class="mt-1 text-xs text-slate-600">(2018 - 2022)</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
.background-hero {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(to bottom, rgba(253, 250, 245, 0) 90%, rgba(253, 250, 245, 0.1) 10%, rgba(253, 250, 245, 1) 100%), url('@/assets/img/sky-transparent-bg.jpg');
  background-size: cover;
  background-position: center;
  z-index: -1;
}

section {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>