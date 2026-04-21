<template>
  <section
    class="relative col-span-12 grid min-h-[500px] grid-cols-12 gap-x-4 gap-y-0 overflow-hidden py-16 text-slate-800">
    <div class="background-hero"></div>
    <div class="relative z-10 col-start-2 col-span-10 grid lg:grid-cols-[50%_50%]">
      <div class="flex flex-col justify-center">
        <h2 class="mb-6 text-2xl font-[Perpetua] uppercase md:text-3xl text-[var(--color-text-red)]">
          My approach
        </h2>

        <div class="space-y-6 text-balance font-[roboto]">
          <p class="text-sm leading-relaxed text-slate-700">
            I aim to design for people, not just screens, anchoring my workflow in user
            research to build solutions as functional as they are beautiful.
          </p>

          <p class="text-sm leading-relaxed text-slate-700">
            As a good listener with a highly empathetic and organized mindset, I focus on
            structure and usability.
          </p>

          <p class="text-sm leading-relaxed text-slate-700">
            I truly love helping people and aim to create tools that make lives easier.
          </p>
        </div>
      </div>

      <div
        class="my-4 md:ml-6 flex h-fit flex-col justify-center rounded-[24px] border border-white/30 bg-white/20 p-5 font-[roboto] backdrop-blur-lg sm:my-5 md:mt-6 lg:mt-16 lg:items-start">
        <h2 class="mb-6 text-2xl font-[Perpetua] uppercase md:text-3xl text-[var(--color-text-red)]">
          Tools I Use
        </h2>

        <div class="flex flex-row flex-wrap gap-4 w-fit">

          <img src="@/assets/svg/html-icon.svg" alt="HTML">
          <img src="@/assets/svg/css-icon.svg" alt="CSS">
          <img src="@/assets/svg/js-icon.svg" alt="JavaScript">
          <img src="@/assets/svg/vue-icon.svg" alt="Vue.js">
          <img src="@/assets/svg/tailwind-icon.svg" alt="Tailwind CSS">
          <img src="@/assets/svg/github.svg" alt="GitHub">




          <img src="@/assets/svg/illustrator-icon.svg" alt="Illustrator">
          <img src="@/assets/svg/photoshop-icon.svg" alt="Photoshop">
          <img src="@/assets/svg/figma-icon.svg" alt="Figma">
          <img src="@/assets/svg/premierepro-icon.svg" alt="Premiere Pro">
          <img src="@/assets/svg/indesign-icon.svg" alt="InDesign">
          <img src="@/assets/svg/canva-icon.svg" alt="Canva">




          <img src="@/assets/svg/notion-icon.svg" alt="Notion">
          <img src="@/assets/svg/microsoft-icon.svg" alt="Microsoft Office">



        </div>
      </div>
    </div>
  </section>
</template>

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
}

img {
  width: 36px;
  height: 36px;
  opacity: 0.9;
  margin: 0.3rem;
}
</style>