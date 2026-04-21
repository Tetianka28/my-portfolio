<script setup>

</script>

<template>
  <section class="mt-10 min-h-screen font-roboto text-slate-800 sm:mt-12 lg:mt-15">
    
    <header class="mb-10 sm:mb-12">
      <div class="mb-4 flex items-center gap-4 uppercase text-[11px] font-[roboto] font-medium text-slate-600 sm:text-xs">
        <span class="border-b-2 border-slate-600 pb-1">Value Hypothesis Case Study </span>
      </div>
      
      <h1 class="mb-6 font-perpetua text-2xl uppercase text-[var(--color-text-red)] sm:mb-8 sm:text-3xl lg:text-4xl">
        Theater Production Management App — <span class="font-light">UI/UX Case Study</span>
      </h1>

      <p class="mb-5 font-[roboto] text-base leading-7 text-slate-700 sm:mb-6 sm:text-lg sm:leading-relaxed">
        This project started as part of a UX assignment, but I wanted to approach it as something real — not just invent a random app idea. 
        I was interested in how people manage messy, collaborative work in real life, so I focused on small theatre groups. 
        They often work in a very hands-on, informal way, but still have to coordinate a lot of moving parts.</p>
       <h3 class="lg:mb-10 font-[roboto] text-base leading-7 text-slate-700 sm:mb-4 sm:text-lg sm:leading-relaxed">Role: UX Researcher</h3>


      <div class="flex flex-col gap-8 sm:gap-10 md:flex-row md:items-center md:gap-16 lg:gap-32">
         <button class="rounded bg-blue/60 p-4 shadow-lg shadow-red-400/20 backdrop-blur-sm sm:p-5 lg:p-6">
           <a href="https://www.figma.com/board/DElaAn9VOJk93uJUjRdsDa/UX-Project-APP?node-id=0-1&t=IAWZwFxzwoe9KTlt-1" 
           target="_blank" class="font-medium font-[roboto] text-sm text-slate-700 sm:text-base">FigJam Link</a>
        </button>
         <button class="rounded bg-blue/60 p-4 shadow-lg shadow-red-400/20 backdrop-blur-sm sm:p-5 lg:p-6">
            <a href="https://www.figma.com/design/gug6yqhEYLTFyuyiDuxfnT/UX-Project-APP?node-id=0-1&t=IAWZwFxzwoe9KTlt-1" 
            target="_blank" rel="noopener noreferrer" class="font-medium font-[roboto] text-sm text-slate-700 sm:text-base">
            View Prototype
            </a>
        </button>

        
        <div class="flex flex-wrap items-center gap-4 sm:gap-6">
          <h3 class="font-medium font-[roboto] text-sm uppercase sm:text-base">Tools</h3>
          <div id="tools-used" class="flex flex-row gap-3 sm:gap-4">
            <img src="@/assets/svg/illustrator-icon.svg" alt="Illustrator Icon" class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
            <img src="@/assets/svg/figma-icon.svg" alt="Figma Icon" class="h-7 w-7 object-contain sm:h-8 sm:w-8 lg:h-9 lg:w-9">
          </div>
        </div>

      </div>
    </header>

    <div class="mt-12 grid gap-6 sm:mt-14 md:grid-cols-2 md:gap-8 lg:mt-16">
      
      <div class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2 class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">Problem statement</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>Small theatre teams rely on multiple disconnected tools to manage their work, leading to confusion, inefficiency, and 
            unnecessary complexity. Existing solutions are often too generic or overwhelming, forcing users to adapt their workflows 
            instead of supporting them. This makes it harder to coordinate tasks, access relevant information, and collaborate effectively.
          </p>
          <p>There is a need for a simple, centralized, and role-adaptive solution that reduces 
            cognitive load and better supports the way small theatre productions actually work.
          </p>
          
        </div>
      </div>

      <div class="rounded-[28px] border border-white/20 bg-[#FAF2E5]/40 p-5 font-[roboto] shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm sm:rounded-[32px] sm:p-6 lg:rounded-[40px] lg:p-8">
        <h2 class="mb-5 border-b-1 border-[var(--color-red)] pb-2 text-center font-roboto text-sm font-medium uppercase text-slate-700 sm:mb-6 sm:text-base">Solution</h2>
        <div class="space-y-4 text-sm text-slate-800 sm:text-[15px]">
          <p>Based on the research and early direction, I designed a concept for a mobile app that acts as a shared workspace for theatre productions.</p>
          <div class="space-y-3">
            <p>The goal wasn’t to create something complex, but something that feels clear, structured, and easy to navigate — even for users who aren’t very comfortable with digital tools.</p>
            <p>Visually, I chose a red, blue, and off-white color scheme. It connects to the theatre context but also keeps enough contrast to stay readable and comfortable for different age groups.</p>
          </div>
        </div>
      </div>

      <!-- <div class="mt-4 md:col-span-2 md:mt-6 lg:mt-8 flex align-middle justify-start gap-6">
      </div> -->
    </div>
  </section>
</template>

<style scoped>

.font-perpetua {
  font-family: 'Perpetua', serif;
}
</style>