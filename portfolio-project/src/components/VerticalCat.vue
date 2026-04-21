<template>
  <aside>
    <h2 class="text-xl font-base text-slate-700 mb-4 font-[roboto]">My works by categories</h2>
    <ul class="flex flex-row flex-wrap gap-3 lg:flex-col lg:gap-3">
      <li v-for="category in categories" :key="category">
        <button
          type="button"
          @click="setCategory(category)"
          :aria-pressed="modelValue === category"
          :class="[
            'w-auto rounded-2xl px-7 py-2 text-center text-sm font-[roboto] font-normal transition-all duration-200 lg:w-full lg:px-4 lg:py-3',
            modelValue === category
              ? 'bg-[var(--color-red)] text-white shadow-[0_10px_20px_rgba(187,212,234,0.45)]'
              : 'bg-[#BBD4EA] text-[var(--color-red)] hover:bg-slate-200 shadow-[0_10px_20px_rgba(163,13,13,0.35)] [text-shadow:0_0_4px_rgba(255,255,255,0.85),0_0_10px_rgba(255,255,255,0.45)]'
          ]"
        >
          {{ category }}
        </button>
      </li>
    </ul>
  </aside>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue'

const props = defineProps({
  categories: {
    type: Array,
    default: () => [],
  },
  modelValue: {
    type: String,
    default: '',
  },
})

const emit = defineEmits(['update:modelValue'])

function setCategory(category) {
  emit('update:modelValue', category)
}
</script>

<style scoped>
</style>
