<script setup>

</script>

<template>
  <section class="mt-10 min-h-screen font-roboto text-slate-800 sm:mt-12 lg:mt-15">
    
    <header class="mb-10 sm:mb-12">
      <div class="mb-4 flex items-center gap-4 uppercase text-[11px] font-[roboto] font-medium text-slate-600 sm:text-xs">
        <span class="border-b-2 border-slate-600 pb-1">Poster for Print and Web</span>
      </div>
      
      <h1 class="mb-6 font-perpetua text-2xl uppercase text-[var(--color-text-red)] sm:mb-8 sm:text-3xl lg:text-4xl">
        International Day Poster
      </h1>

      <p class="mb-5 font-[roboto] text-base leading-7 text-slate-700 sm:mb-6 sm:text-lg sm:leading-relaxed">
        International Day event at my academy brought together students from different countries to present their food, drinks, 
        traditional clothing, and culture. The poster needed to communicate this clearly while standing out in a busy student environment.
      </p>
      <p class="mb-8 font-[roboto] text-base leading-7 text-slate-700 sm:mb-10 sm:text-lg sm:leading-relaxed">
        Goal: Create a visually appealing and easy-to-understand poster to attract students to participate in an international cultural event.
      </p>

      <div class="flex flex-col gap-8 sm:gap-10 md:flex-row md:items-center md:gap-16 lg:gap-32">
        <div class="rounded bg-blue/60 p-4 shadow-lg shadow-red-400/20 backdrop-blur-sm sm:p-5 lg:p-6">
          <h3 class="font-medium font-[roboto] text-sm text-slate-700 sm:text-base">Role: Graphic Designer</h3>
        </div>
        
        <div class="flex flex-wrap items-center gap-4 sm:gap-6">
          <h3 class="font-medium font-[roboto] text-sm uppercase sm:text-base">Tools</h3>
          <div id="tools-used" class="flex flex-row gap-3 sm:gap-4">
            <img src="@/assets/svg/indesign-icon.svg" alt="InDesign Icon" class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
            <img src="@/assets/svg/illustrator-icon.svg" alt="Illustrator Icon" class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
            <img src="@/assets/svg/photoshop-icon.svg" alt="Photoshop Icon" class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
          </div>
        </div>
      </div>
    </header>

    <div class="mt-12 grid gap-6 sm:mt-14 md:grid-cols-2 md:gap-8 lg:mt-16">
      
      <div class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2 class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">Problem Statement</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>Students are often exposed to many posters and announcements daily, which leads to:</p>
          <ul class="list-disc ml-6 space-y-2">
            <li>Information overload</li>
            <li>Low engagement with event promotions</li>
            <li>Skimming instead of reading</li>
          </ul>
          <p>Challenge: How might I design a poster that quickly captures attention while clearly communicating the purpose of the event?</p>
        </div>
      </div>

      <div class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2 class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">Solution</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>I developed a metaphor-based concept: </p>
          <p>“Your plate” = Your identity, your culture, your contribution. This makes the poster:</p>
          <div class="space-y-3">
            <p><span class="font-medium">Interactive</span> (mentally engaging the viewer)</p>
            <p><span class="font-medium">Inclusive</span>(everyone is invited to contribute)</p>
            <p><span class="font-medium">Easy to understand at a glance</span></p>
          </div>
        </div>
      </div>

      <div class="mt-4 md:col-span-2 md:mt-6 lg:mt-8 flex align-middle justify-center gap-6">
        <img src="@/assets/img/international-day.webp" alt="international-day-poster-final-design" class="w-full max-w-[220px] rounded-lg shadow-lg sm:max-w-[280px] md:max-w-[320px] lg:max-w-[800px]">
      </div>
    </div>
  </section>
</template>

<style scoped>

.font-perpetua {
  font-family: 'Perpetua', serif;
}
</style>