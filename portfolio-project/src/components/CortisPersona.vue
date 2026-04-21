<script setup>

</script>

<template>
  <section class="mt-10 min-h-screen font-roboto text-slate-800 sm:mt-12 lg:mt-15">
    
    <header class="mb-10 sm:mb-12">
      <div class="mb-4 flex items-center gap-4 uppercase text-[11px] font-[roboto] font-medium text-slate-600 sm:text-xs">
        <span class="border-b-2 border-slate-600 pb-1">BUILDING A PERSONA</span>
      </div>
      
      <h1 class="mb-6 font-perpetua text-2xl uppercase text-[var(--color-text-red)] sm:mb-8 sm:text-3xl lg:text-4xl">
        CORTIS - Website User Persona
      </h1>

      <p class="mb-5 font-[roboto] text-base leading-7 text-slate-700 sm:mb-6 sm:text-lg sm:leading-relaxed">
        The project is a fictional case with the focus on building a user-centered foundation before designing. 
        Instead of jumping into visuals, I focused on understanding how fans actually behave, what they expect, and what frustrates them.
      </p>
      <p class="font-[roboto] text-base leading-7 text-slate-700 sm:mb-6 sm:text-lg sm:leading-relaxed">Role: UX Researcher</p>


      <div class="flex flex-col gap-8 sm:gap-10 md:flex-row md:items-center md:gap-16 lg:gap-32">
        
        <button class="rounded bg-blue/60 p-4 shadow-lg shadow-red-400/20 backdrop-blur-sm sm:p-5 lg:p-6">
           <a href="https://www.figma.com/board/RpIrwklvRY7ClpZ364jm15/CORTIS---Persona?t=IAWZwFxzwoe9KTlt-1" 
           target="_blank" class="font-medium font-[roboto] text-sm text-slate-700 sm:text-base">Figma Link</a>
        </button>
        
        <div class="flex flex-wrap items-center gap-4 sm:gap-6">
          <h3 class="font-medium font-[roboto] text-sm uppercase sm:text-base">Tools</h3>
          <div id="tools-used" class="flex flex-row gap-3 sm:gap-4">
            <img src="@/assets/svg/figma-icon.svg" alt="Figma Icon" class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
          </div>
        </div>
      </div>
    </header>

    <div class="mt-12 grid gap-6 sm:mt-14 md:grid-cols-2 md:gap-8 lg:mt-16">
      
      <div class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2 class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">My approach</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>To avoid making assumptions, I conducted informal interviews with 2 users who actively listen to music and engage with artists online. Method:</p>
          <ul class="list-disc ml-6 space-y-2">
            <li>Short structured interview</li>
            <li>Open-ended questions about habits, frustrations, and expectations</li>
            <li>Focus on real behavior, not ideal scenarios</li>
          </ul>
        </div>
      </div>

      <div class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2 class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">Why this matters</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>This project helped me understand that:</p>
         <ul class="list-disc ml-6 space-y-2">
            <li>Users don’t just want features — they want clarity and trust</li>
            <li>Not all users behave the same (important for feature decisions)</li>
            <li>Emotional connection is just as important as functionality in fan-based products</li>
          </ul>
        </div>
      </div>

      <div class="mt-4 md:col-span-2 md:mt-6 lg:mt-8 flex align-middle justify-start gap-6">
        <img src="@/assets/img/persona-interview.png" alt="CORTIS Persona interview" class="hidden w-full max-w-[220px] rounded-lg shadow-lg lg:block lg:max-w-[700px]">
      </div> 


    </div>
  </section>
</template>

<style scoped>

.font-perpetua {
  font-family: 'Perpetua', serif;
}
</style>