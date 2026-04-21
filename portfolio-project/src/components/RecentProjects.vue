<template>
  <section class="">
    <div class="mx-auto mb-15">
      <div class="mb-8">
        <h2 class="text-4xl font-[perpetua] uppercase">Recent Projects</h2>
      </div>

      <div class="mb-8 flex flex-wrap gap-3">
        <button
          v-for="category in categories"
          :key="category"
          @click="setCategory(category)"
          :class="[
            'rounded-lg px-7 py-2 text-sm font-[roboto] font-normal transition-all duration-200',
            activeCategory === category
              ? 'bg-[var(--color-red)] text-white shadow-[0_10px_20px_rgba(187,212,234,0.45)]'
              : 'bg-[#BBD4EA] text-[var(--color-red)] hover:bg-slate-200 shadow-[0_10px_20px_rgba(163,13,13,0.35)] [text-shadow:0_0_4px_rgba(255,255,255,0.85),0_0_10px_rgba(255,255,255,0.45)]',
          ]"
        >
          {{ category }}
        </button>
      </div>

      <TransitionGroup
        name="fade"
        tag="div"
        class="grid gap-6 md:grid-cols-2"
      >
        <div
          v-for="project in filteredProjects"
          :key="project.id"
          class="group rounded-[24px] border border-white/30 p-5 font-[roboto] backdrop-blur-lg bg-[#FAF2E5]/60 shadow-[0_18px_35px_rgba(163,13,13,0.18)] transition-all duration-300 hover:-translate-y-1 hover:scale-[1.02] hover:shadow-[0_22px_55px_rgba(163,13,13,0.16)]"
        >
          <div class="text-[9px] font-medium uppercase text-[var(--color-text-red)]">
            {{ project.category }}
          </div>
          <h3 class="mt-2.5 text-[1.35rem] font-[roboto] leading-tight text-slate-700">{{ project.title }}</h3>
          <div class="my-4 h-[2px] w-10 bg-[var(--color-text-red)]"></div>
          <p class="text-base font-[roboto] leading-6 text-slate-700 line-clamp-4">{{ project.desc }}</p>
          <button
            type="button"
            class="mt-5 inline-flex font-[roboto] items-center gap-1.5 text-[13px] font-normal uppercase text-[var(--color-text-red)] cursor-pointer"
            @click="openProject(project)"
          >
            <span>View Project</span>
            <svg class="h-3.5 w-3.5 transition-transform duration-200 group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </button>
        </div>
      </TransitionGroup>

    </div>
  </section>
</template>

<script setup>
import { computed, ref } from 'vue'
import { useRouter } from 'vue-router'
import { projectCategories, projectSlides } from '@/data/projectSlides'

const router = useRouter()
const categories = projectCategories
const activeCategory = ref('UX CASES')

const filteredProjects = computed(() => {
  if (activeCategory.value === 'ALL') {
    return projectSlides.slice(0, 2)
  }

  return projectSlides.filter((project) => project.category === activeCategory.value).slice(0, 2)
})

function setCategory(category) {
  if (category === 'ALL') {
    router.push('/projects')
    return
  }

  activeCategory.value = category
}

function openProject(project) {
  router.push({
    name: 'projects',
    query: {
      project: String(project.id),
    },
  })
}
</script>

<style scoped>
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(12px);
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.25s ease, transform 0.25s ease;
}
</style>
