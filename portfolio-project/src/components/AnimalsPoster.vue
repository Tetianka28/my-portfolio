<script setup>

</script>

<template>
  <section class="mt-10 min-h-screen font-roboto text-slate-800 sm:mt-12 lg:mt-15">

    <header class="mb-10 sm:mb-12">
      <div
        class="mb-4 flex items-center gap-4 uppercase text-[11px] font-[roboto] font-medium text-slate-600 sm:text-xs">
        <span class="border-b-2 border-slate-600 pb-1">Infographics Poster</span>
      </div>

      <h1 class="mb-6 font-perpetua text-2xl uppercase text-[var(--color-text-red)] sm:mb-8 sm:text-3xl lg:text-4xl">
        Animal Rescue Mission — <span class="font-light">UX Case Study</span>
      </h1>

      <p class="mb-5 font-[roboto] text-base leading-7 text-slate-700 sm:mb-6 sm:text-lg sm:leading-relaxed">
        This poster was created as part of a design challenge focused on raising awareness through infographics with
        data.
        The topic addressed the impact of the war in Ukraine on animal shelters and stray populations.
      </p>
      <p class="mb-8 font-[roboto] text-base leading-7 text-slate-700 sm:mb-10 sm:text-lg sm:leading-relaxed">
        Goal: Communicate the growing crisis of animal overpopulation in shelters and encourage students to take action.
      </p>

      <div class="flex flex-col gap-8 sm:gap-10 md:flex-row md:items-center md:gap-16 lg:gap-32">
        <div class="rounded bg-blue/60 p-4 shadow-lg shadow-red-400/20 backdrop-blur-sm sm:p-5 lg:p-6">
          <h3 class="font-medium font-[roboto] text-sm text-slate-700 sm:text-base">Role: UX/UI Designer</h3>
        </div>

        <div class="flex  items-center gap-4 sm:gap-6">
          <h3 class="font-medium font-[roboto] text-sm uppercase sm:text-base">Tools</h3>
          <div id="tools-used" class="flex flex-row gap-3 sm:gap-4">
            <img src="@/assets/svg/indesign-icon.svg" alt="InDesign Icon"
              class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
            <img src="@/assets/svg/illustrator-icon.svg" alt="Illustrator Icon"
              class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
            <img src="@/assets/svg/photoshop-icon.svg" alt="Photoshop Icon"
              class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
          </div>
        </div>
      </div>
    </header>

    <div class="mt-12 grid gap-6 sm:mt-14 md:grid-cols-2 md:gap-8 lg:mt-16">

      <div
        class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2
          class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">
          Problem Statement</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>Raising awareness about serious issues through posters is difficult because:</p>
          <ul class="list-disc ml-6 space-y-2">
            <li>Viewers often don’t engage with dense or data-heavy visuals</li>
            <li>Important statistics are ignored if not clearly structured</li>
            <li>Emotional topics require both clarity and empathy</li>
          </ul>
        </div>
      </div>

      <div
        class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2
          class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">
          Solution</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>The design solves the challenge of presenting complex, emotionally sensitive information by making it
            clear, structured, and engaging:</p>
          <div class="space-y-3">
            <p><span class="font-medium">Progressive Disclosure:</span> Information is revealed step-by-step to support
              easier understanding.</p>
            <p><span class="font-medium">Visual Hierarchy:</span> Typography and color guide attention to the most
              important content.</p>
            <p><span class="font-medium">Emotional Design:</span> Imagery builds empathy before presenting factual
              information.</p>
          </div>
        </div>
      </div>

      <div class="mt-4 md:col-span-2 md:mt-6 lg:mt-8 flex align-middle justify-center gap-6">
        <img src="@/assets/img/animals-poster.webp" alt="rescue-animals-poster-final-design"
          class="w-full max-w-[220px] rounded-lg shadow-lg sm:max-w-[280px] md:max-w-[320px] lg:max-w-[360px]">
        <img src="@/assets/img/animals-poster-mockup.webp" alt="rescue-animals-poster-mockup-final-design"
          class="w-full max-w-[220px] rounded-lg shadow-lg sm:max-w-[280px] md:max-w-[320px] lg:max-w-[360px]">
      </div>
    </div>
  </section>
</template>

<style scoped>
.font-perpetua {
  font-family: 'Perpetua', serif;
}
</style>