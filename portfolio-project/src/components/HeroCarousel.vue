<script setup>
import { computed, ref, watch } from 'vue'
import { projectSlides } from '@/data/projectSlides'

const emit = defineEmits(['select-project'])

const props = defineProps({
  selectedCategory: {
    type: String,
    default: 'ALL',
  },
})
const slides = ref(projectSlides)

const activeIndex = ref(0)

const visibleSlides = computed(() => {
  if (props.selectedCategory === 'ALL') {
    return slides.value
  }

  return slides.value.filter((slide) => slide.category === props.selectedCategory)
})

watch(
  visibleSlides,
  () => {
    activeIndex.value = 0
  },
)

const nextSlide = () => {
  if (visibleSlides.value.length <= 1) {
    return
  }

  activeIndex.value = (activeIndex.value + 1) % visibleSlides.value.length
}

const prevSlide = () => {
  if (visibleSlides.value.length <= 1) {
    return
  }

  activeIndex.value = (activeIndex.value - 1 + visibleSlides.value.length) % visibleSlides.value.length
}
</script>

<template>
  <div class="background-hero"></div>
  <div class="relative w-full mx-auto h-[340px] rounded-2xl flex flex-col items-center justify-center">

    <button 
      @click="prevSlide" 
      class="absolute top-1 left-1/2 z-10 flex h-12 w-12 -translate-x-1/2 items-center justify-center rounded-full bg-white/30 text-2xl text-[var(--color-text-red)] shadow-md backdrop-blur-sm"
      aria-label="Previous Slide"
    >
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="m4.5 15.75 7.5-7.5 7.5 7.5" />
      </svg>
    </button>

    <div class="relative h-full w-full overflow-hidden">
        <div 
          class="flex h-full w-full flex-col transition-transform duration-700 ease-out will-change-transform"
          :style="{ transform: `translateY(-${activeIndex * 100}%)` }"
        >
          <div 
            v-for="slide in visibleSlides" 
            :key="slide.id" 
            class="h-full min-h-full w-full shrink-0 px-5 py-5"
          >
            <div class="flex h-full w-full overflow-hidden rounded-[40px] bg-[#FAF2E5]/60 shadow-[0_18px_35px_rgba(163,13,13,0.18)] backdrop-blur-sm min-[900px]:flex-row">
              
              <div class="w-full pt-10 px-8 pb-6 flex flex-col items-start font-[roboto] min-[900px]:w-[70%]">
                 <h2 class="text-xl font-normal uppercase text-slate-800 mb-2">{{ slide.title }}</h2>
                 <h3 class="text-sm text-slate-500 mb-3">{{ slide.category }}</h3>
                 <p class="text-slate-700 text-sm lg:text-base mb-4 line-clamp-3 leading-relaxed">{{ slide.desc }}</p>
                 <button class="bg-[var(--color-red)] text-white text-sm px-4 py-2 mb-4 sm:mb-2 md:mb-2 rounded-lg opacity-80 hover:opacity-100 transition-opacity" @click="emit('select-project', slide)">See details</button>
              </div>
              <div class="hidden h-full w-full min-[900px]:block min-[900px]:w-[30%] min-[900px]:max-w-[30%] min-[900px]:flex-shrink-0">
                <img :src="slide.img" class="h-full w-full object-cover" />
              </div>
              
            </div>
          </div>
        </div>
    </div>

    <button 
      @click="nextSlide" 
      class="absolute bottom-1 left-1/2 z-10 flex h-12 w-12 -translate-x-1/2 items-center justify-center rounded-full bg-white/30 text-2xl text-[var(--color-text-red)] shadow-md backdrop-blur-sm"
      aria-label="Next Slide"
    >
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
      </svg>
    </button>
  </div>
</template>

<style>
.background-hero {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(to bottom, rgba(253, 250, 245, 0) 0%, rgba(253, 250, 245, 0.1) 70%, rgba(253, 250, 245, 1) 100%), url('@/assets/img/hero-bg.jpg');
  background-size: cover;
  background-position: center;
  z-index: -1;
}
</style>

