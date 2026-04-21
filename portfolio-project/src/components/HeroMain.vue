<script setup>
const emit = defineEmits(['next-slide'])

function handleAboutClick() {
  emit('next-slide')
}
</script>

<template>
  <section class="col-span-12 grid min-h-[500px] grid-cols-12 gap-x-4 gap-y-0 overflow-hidden relative">
    <div class="background-hero"></div>
    <div class="col-start-2 col-span-7 hero-left relative z-10 font-[roboto] my-[97px]">
      <h1 class="font-[perpetua] text-4xl uppercase mb-3">PORTFOLIO</h1>
      <h2 class="text-black-lg opacity-50 mb-4">UI-DESIGNER | UX-RESEARCHER | FRONTEND DEVELOPER</h2>
      <p class="text-base mb-8 leading-relaxed text-slate-700">I am a UX/UI design student currently diving deep into the world of front-end development. My focus is on learning how to turn well-researched ideas into clean, functional code with Vue and Tailwind. I’m a big fan of organized structures and usability, and I’m currently spending my time refining my technical workflow to build digital tools that actually work the way they’re supposed to.</p>
      <button type="button" class="shiny-button" @click="handleAboutClick">
        ABOUT ME
      </button>
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
</style> 