<script setup>
import { computed, nextTick, ref, watch } from 'vue'
import { useRoute, useRouter } from 'vue-router'
import HeroCarousel from '@/components/HeroCarousel.vue'
import VerticalCat from '@/components/VerticalCat.vue'
import Footer from '@/components/Footer.vue'
import AnimalsPoster from '@/components/AnimalsPoster.vue'
import { projectCategories, projectSlides } from '@/data/projectSlides'
import RacingProject from '@/components/RacingProject.vue'
import TheaterProject from '@/components/TheaterProject.vue'
import InterDayPoster from '@/components/InterDayPoster.vue'
import CortisPersona from '@/components/CortisPersona.vue'
import YummyProject from '@/components/YummyProject.vue'


const route = useRoute()
const router = useRouter()
const categories = projectCategories
const activeCategory = ref('ALL')
const selectedProject = ref(null)
const detailSection = ref(null)

function getProjectComponent(project) {
  if (!project) {
    return null
  }

  if (project.title === 'Animal Rescue Mission') {
    return AnimalsPoster
  }

  if (project.title === '230 RACING - Building a brand identity') {
    return RacingProject
  }

  if (project.title === 'Theater Production Management App') {
    return TheaterProject
  }

  if (project.title === 'International Day Poster') {
    return InterDayPoster
  }

  if (project.title === 'CORTIS Website Persona') {
    return CortisPersona
  }

  if (project.title === 'YUMMY RECIPES - Cooking website UI/UX Case Study') {
    return YummyProject
  }

  return null
}

function clearProjectQuery() {
  if (!route.query.project) {
    return
  }

  const nextQuery = { ...route.query }
  delete nextQuery.project

  router.replace({ name: 'projects', query: nextQuery })
}

const selectedProjectComponent = computed(() => {
  return getProjectComponent(selectedProject.value)
})

async function handleProjectSelect(project) {
  activeCategory.value = project.category
  selectedProject.value = project

  if (route.query.project !== String(project.id)) {
    router.replace({
      name: 'projects',
      query: {
        ...route.query,
        project: String(project.id),
      },
    })
  }

  await nextTick()
  detailSection.value?.scrollIntoView({ behavior: 'smooth', block: 'start' })
}

function closeProjectDetails() {
  selectedProject.value = null
  clearProjectQuery()
}

watch(activeCategory, (category) => {
  if (!selectedProject.value || selectedProject.value.category === category) {
    return
  }

  selectedProject.value = null
  clearProjectQuery()
})

watch(
  () => route.query.project,
  async (projectId) => {
    if (!projectId) {
      selectedProject.value = null
      return
    }

    const project = projectSlides.find((slide) => String(slide.id) === String(projectId))

    if (!project || !getProjectComponent(project)) {
      selectedProject.value = null
      clearProjectQuery()
      return
    }

    activeCategory.value = project.category
    selectedProject.value = project

    await nextTick()
    detailSection.value?.scrollIntoView({ behavior: 'smooth', block: 'start' })
  },
  { immediate: true },
)
</script>

<template>
  <div class="">
    <div class="grid grid-cols-12 gap-4 overflow-hidden">
      <div class="col-start-2 col-span-10 mt-16">
        <div class="">

          <div class="grid gap-10 lg:grid-cols-[280px_1fr]">

            <VerticalCat :categories="categories" v-model="activeCategory" />
            <HeroCarousel :selected-category="activeCategory" @select-project="handleProjectSelect" />

          </div>

        </div>




      </div>
      <section
        v-if="selectedProjectComponent"
        class="col-span-12 bg-[linear-gradient(to_bottom,rgba(253,250,245,1)_10%,rgba(253,250,245,0.2)_20%,rgba(253,250,245,0)_100%),url('@/assets/img/sky-transparent-bg.jpg')] bg-cover bg-center"
      >
        <div ref="detailSection" class="grid grid-cols-12 gap-x-4 gap-y-0">
          <div class="col-start-2 col-span-10">
            <div class="flex items-center justify-between gap-6 pt-16">
              <div>
                <p class="text-xs font-[roboto] uppercase text-[var(--color-text-red)]">Selected project</p>
              </div>

              <button
                type="button"
                class="rounded-2xl border border-white/20 bg-[#FAF2E5]/50 px-5 py-2 font-[roboto] text-sm uppercase text-[var(--color-red)] shadow-[0_10px_20px_rgba(163,13,13,0.18)] backdrop-blur-sm transition-opacity hover:opacity-80"
                @click="closeProjectDetails"
              >
                Close
              </button>
            </div>

            <component :is="selectedProjectComponent" />
          </div>
        </div>

        <Footer />
      </section>

      <Footer v-else class="col-span-12" />

    </div>
  </div>

</template>

<!--overflow-hidden rounded-[40px] bg-[linear-gradient(to_bottom,rgba(253,250,245,0.08)_0%,rgba(253,250,245,0.32)_100%),url('@/assets/img/sky-transparent-bg.jpg')] bg-cover bg-center px-6 py-8 lg:px-10 lg:py-10-->