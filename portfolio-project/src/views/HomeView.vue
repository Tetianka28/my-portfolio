<script setup>
import { ref } from 'vue'
import HeroMain from '../components/HeroMain.vue'
import HeroSecond from '../components/HeroSecond.vue'
import HeroThird from '../components/HeroThird.vue'
import RecentProjects from '../components/RecentProjects.vue'
import Footer from '@/components/Footer.vue'

const slides = [
  { id: 'hero-main', component: HeroMain },
  { id: 'hero-second', component: HeroSecond },
  { id: 'hero-third', component: HeroThird },
]
const activeSlide = ref(0)

function goToSlide(index) {
  activeSlide.value = index
}

function goToNextSlide() {
  activeSlide.value = (activeSlide.value + 1) % slides.length
}

function goToPreviousSlide() {
  activeSlide.value = (activeSlide.value - 1 + slides.length) % slides.length
}
</script>

<template>  
  <div class="wrapper grid grid-cols-12 gap-x-4 gap-y-0">
    <section class="col-span-12 relative">
      <div class="overflow-hidden">
        <div
          class="flex transition-transform duration-700 ease-in-out"
          :style="{ transform: `translateX(-${activeSlide * 100}%)` }"
        >
          <div
            v-for="slide in slides"
            :key="slide.id"
            class="w-full shrink-0"
          >
            <div class="grid grid-cols-12 gap-x-4 gap-y-0">
              <component :is="slide.component" @next-slide="goToNextSlide" />
            </div>
          </div>
        </div>
      </div>

      <button
        v-if="activeSlide > 0"
        type="button"
        class="absolute left-6 top-1/2 z-20 flex h-12 w-12 -translate-y-1/2 items-center justify-center rounded-full bg-white/60 text-2xl text-[var(--color-text-red)] shadow-md backdrop-blur-sm"
        @click="goToPreviousSlide"
        aria-label="Previous slide"
      >
        <span aria-hidden="true">&lsaquo;</span>
      </button>

      <button
        v-if="activeSlide > 0"
        type="button"
        class="absolute right-6 top-1/2 z-20 flex h-12 w-12 -translate-y-1/2 items-center justify-center rounded-full bg-white/60 text-2xl text-[var(--color-text-red)] shadow-md backdrop-blur-sm"
        @click="goToNextSlide"
        aria-label="Next slide"
      >
        <span aria-hidden="true">&rsaquo;</span>
      </button>

      <div class="absolute bottom-8 left-1/2 z-20 flex -translate-x-1/2 gap-3">
        <button
          v-for="(slide, index) in slides"
          :key="`indicator-${slide.id}`"
          type="button"
          class="h-2.5 rounded-full transition-all duration-300"
          :class="activeSlide === index ? 'w-10 bg-[var(--color-text-red)]' : 'w-2.5 bg-black/25'"
          :aria-label="`Go to slide ${index + 1}`"
          :aria-current="activeSlide === index ? 'true' : 'false'"
          @click="goToSlide(index)"
        />
      </div>
    </section>

    <section class="col-span-12 bg-[linear-gradient(to_top,rgba(253,250,245,0)_0%,rgba(253,250,245,0.1)_60%,rgba(253,250,245,1)_100%),url('@/assets/img/sky-transparent-bg.jpg')] bg-cover bg-center">
      <div class="grid grid-cols-12 gap-x-4 gap-y-0">
        <div class="col-start-2 col-span-10">
         <RecentProjects />
         </div>
      </div>

     <Footer />
   </section>

   
   
  </div>



</template>


<style scoped>

</style>