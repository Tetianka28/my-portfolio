<template>
  <nav ref="navRef" class="nav-glass px-4 sm:px-6 lg:px-8">
    <div class="mx-auto flex min-h-[80px] w-full max-w-7xl items-center justify-between gap-4">
      <button @click="handleLogoClick" type="button" class="flex h-8 shrink-0 items-center sm:h-9 lg:h-10">
        <img src="@/assets/img/logo.png" alt="logo-tania" class="h-full w-auto max-w-none object-contain shrink-0" />
      </button>

      <div class="hidden items-center gap-5 text-sm md:flex lg:gap-8">
        <button @click="handleLogoClick" type="button" class="transition-opacity hover:opacity-70">HOME</button>
        <button @click="scrollToFooter" type="button" class="transition-opacity hover:opacity-70 uppercase">Get in touch</button>
        <RouterLink to="/projects" class="transition-opacity hover:opacity-70">Projects</RouterLink>

        <div class="relative">
          <button
            type="button"
            class="rounded-2xl border bg-[var(--color-dark)] px-7 py-2 text-white transition-transform hover:scale-[1.01] uppercase"
            :aria-expanded="isResumeMenuOpen ? 'true' : 'false'"
            aria-haspopup="true"
            @click="toggleResumeMenu"
          >
            Resume
          </button>

          <div
            v-if="isResumeMenuOpen"
            class="absolute right-0 top-[calc(100%+0.75rem)] z-50 flex min-w-[190px] flex-col gap-2 rounded-[24px] border border-white/30 bg-[#FAF2E5]/30 p-3 shadow-2xl backdrop-blur-md"
          >
            <a
              :href="resumePdfHref"
              target="_blank"
              rel="noreferrer"
              class="rounded-2xl border border-transparent bg-white/65 px-4 py-3 text-center text-sm uppercase text-[var(--color-text-red)] transition-colors hover:bg-white"
              @click="handleResumeLinkClick"
            >
              MY CV.PDF
            </a>
            <a
              href="https://youtu.be/8V4oBUJx8js"
              target="_blank"
              rel="noreferrer"
              class="rounded-2xl border border-transparent bg-white/65 px-4 py-3 text-center text-sm uppercase text-[var(--color-text-red)] transition-colors hover:bg-white"
              @click="handleResumeLinkClick"
            >
              VIDEO CV
            </a>
          </div>
        </div>
      </div>

      <button
        type="button"
        class="inline-flex h-11 w-11 items-center justify-center rounded-2xl border border-white/40 bg-white/35 text-[var(--color-text-red)] backdrop-blur-sm md:hidden"
        :aria-expanded="isMenuOpen ? 'true' : 'false'"
        aria-label="Toggle navigation menu"
        @click="toggleMenu"
      >
        <svg v-if="!isMenuOpen" class="h-5 w-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true">
          <path stroke-linecap="round" d="M4 7h16M4 12h16M4 17h16" />
        </svg>
        <svg v-else class="h-5 w-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 6l12 12M18 6L6 18" />
        </svg>
      </button>
    </div>

    <div v-if="isMenuOpen" class="border-t border-white/30 pb-4 pt-2 md:hidden">
      <div class="flex flex-col gap-2 text-sm">
        <button @click="handleLogoClick" type="button" class="rounded-2xl px-4 py-3 text-left transition-colors hover:bg-white/25">HOME</button>
        <button @click="handleFooterClick" type="button" class="rounded-2xl px-4 py-3 text-left transition-colors hover:bg-white/25 uppercase">Get in touch</button>
        <RouterLink to="/projects" class="rounded-2xl px-4 py-3 transition-colors hover:bg-white/25 uppercase" @click="closeMenu">Projects</RouterLink>

        <div class="flex flex-col gap-2">
          <button
            type="button"
            class="rounded-2xl bg-[var(--color-dark)] px-4 py-3 text-left text-white uppercase"
            :aria-expanded="isResumeMenuOpen ? 'true' : 'false'"
            aria-haspopup="true"
            @click="toggleResumeMenu"
          >
            Resume
          </button>

          <div v-if="isResumeMenuOpen" class="grid gap-2 pl-2">
            <a
              :href="resumePdfHref"
              target="_blank"
              rel="noreferrer"
              class="rounded-2xl border border-white/30 bg-white/45 px-4 py-3 text-left text-xs uppercase text-[var(--color-text-red)] transition-colors hover:bg-white/70"
              @click="handleResumeLinkClick"
            >
              MY CV.PDF
            </a>
            <a
              href="https://www.youtube.com/"
              target="_blank"
              rel="noreferrer"
              class="rounded-2xl border border-white/30 bg-white/45 px-4 py-3 text-left text-xs uppercase text-[var(--color-text-red)] transition-colors hover:bg-white/70"
              @click="handleResumeLinkClick"
            >
              VIDEO CV
            </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { onBeforeUnmount, onMounted, ref, watch } from 'vue'
import { useRoute, useRouter } from 'vue-router'

const isMenuOpen = ref(false)
const isResumeMenuOpen = ref(false)
const navRef = ref(null)
const route = useRoute()
const router = useRouter()
const resumePdfHref = '/my-cv.pdf'
let footerHighlightTriggerTimeoutId = null

watch(
  () => route.fullPath,
  () => {
    closeMenu()
  },
)

onMounted(() => {
  window.addEventListener('pointerdown', handlePointerDown)
})

onBeforeUnmount(() => {
  if (footerHighlightTriggerTimeoutId) {
    window.clearTimeout(footerHighlightTriggerTimeoutId)
  }

  window.removeEventListener('pointerdown', handlePointerDown)
})

function handlePointerDown(event) {
  if (!navRef.value?.contains(event.target)) {
    closeResumeMenu()
  }
}

function scrollToFooter() {
  closeResumeMenu()

  const footer = document.getElementById('footer')
  if (footer) {
    footer.scrollIntoView({ behavior: 'smooth' })

    if (footerHighlightTriggerTimeoutId) {
      window.clearTimeout(footerHighlightTriggerTimeoutId)
    }

    footerHighlightTriggerTimeoutId = window.setTimeout(() => {
      window.dispatchEvent(new Event('highlight-footer'))
      footerHighlightTriggerTimeoutId = null
    }, 700)
  }
}

function scrollToTop() {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value

  if (!isMenuOpen.value) {
    closeResumeMenu()
  }
}

function closeMenu() {
  isMenuOpen.value = false
  closeResumeMenu()
}

function toggleResumeMenu() {
  isResumeMenuOpen.value = !isResumeMenuOpen.value
}

function closeResumeMenu() {
  isResumeMenuOpen.value = false
}

function handleFooterClick() {
  closeMenu()
  scrollToFooter()
}

function handleResumeLinkClick() {
  closeMenu()
}

async function handleLogoClick() {
  closeMenu()

  if (route.name === 'home') {
    scrollToTop()
    return
  }

  await router.push({ name: 'home' })
}
</script>