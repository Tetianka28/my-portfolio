<script setup>
import { onBeforeUnmount, onMounted, ref } from 'vue'

const isHighlighted = ref(false)
let removeHighlightTimeoutId = null

function clearHighlightTimeout() {
    if (removeHighlightTimeoutId) {
        window.clearTimeout(removeHighlightTimeoutId)
        removeHighlightTimeoutId = null
    }
}

function highlightFooter() {
    clearHighlightTimeout()
    isHighlighted.value = true

    removeHighlightTimeoutId = window.setTimeout(() => {
        isHighlighted.value = false
        removeHighlightTimeoutId = null
    }, 1500)
}

onMounted(() => {
    window.addEventListener('highlight-footer', highlightFooter)
})

onBeforeUnmount(() => {
    window.removeEventListener('highlight-footer', highlightFooter)
    clearHighlightTimeout()
})
</script>

<template>
    <section id="footer" class="w-full pt-25">
        <div class="">
            <div class="grid grid-cols-12 gap-y-0 px-4 py-8 md:gap-x-0 lg:gap-x-4 sm:px-0">
                <div
                    class="col-span-12 rounded-[32px] border border-white/20 bg-white/60 p-6 backdrop-blur-sm transition-all duration-500 ease-out sm:col-start-2 sm:col-span-10 sm:rounded-[40px] lg:p-10"
                    :class="isHighlighted ? 'scale-[1.02] shadow-2xl' : 'scale-100 shadow-sm'"
                >
                    <div
                        id="footer-content"
                        class="grid grid-cols-1 gap-0 lg:grid-cols-[45%_10%_45%] lg:gap-0"
                    >
                        <div class="">
                            <h3 class="text-2xl font-bold text-[var(--color-red)] mb-2">Have a project in mind? Let's discuss.</h3>
                            <a href="mailto:tl.tetiana28@gmail.com" class="text-sm font-[roboto] text-[var(--color-dark)] no-underline hover:opacity-80">tl.tetiana28@gmail.com</a>
                            <p class="text-sm font-[roboto] text-[var(--color-dark)]">+45 91 84 96 30</p>

                            <div id="social-links" class="mt-4 flex flex-wrap items-center gap-4">
                                <a href="https://www.linkedin.com/in/tetiana-tarasiuk/" target="_blank" rel="noreferrer" class="text-red-900 transition-opacity hover:opacity-70">
                                    <img src="@/assets/svg/linkedin.svg" alt="linkedin-icon" class="h-7 w-7 footer-social-icon">
                                </a>
                                <a href="https://www.facebook.com/profile.php?id=61555275817100" target="_blank" rel="noreferrer" class="text-red-900 transition-opacity hover:opacity-70">
                                    <img src="@/assets/svg/facebook.svg" alt="facebook-icon" class="h-7 w-7 footer-social-icon">
                                </a>
                                <a href="https://github.com/Tetianka28" target="_blank" rel="noreferrer" class="text-red-900 transition-opacity hover:opacity-70">
                                    <img src="@/assets/svg/github.svg" alt="github-icon" class="h-7 w-7 footer-social-icon">
                                </a>
                                
                            </div>
                        </div>

                        <div class="flex items-center justify-center">
                            <img src="@/assets/img/stars.png" alt="stars-in-footer" class="footer-stars h-20 w-20 object-contain sm:h-24 sm:w-24">
                        </div>

                        <div class="flex flex-col pt-0 lg:ml-9 lg:pt-7">
                            <h3 class="text-sm font-semibold font-[Perpetua] uppercase text-[var(--color-red)]">Note</h3>
                            <p class="font-[roboto] text-xs mb-4 text-[var(--color-dark)]">This portfolio is an evolving collection of my work. I regularly update it with new projects and refinements.</p>
                            <p class="font-[roboto] text-xs text-[var(--color-dark)]">All rights reserved. TANIA 2026</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
.footer-social-icon {
    filter: saturate(1.05);
}
</style>

<!--relative overflow-hidden bg-[url(@/assets/img/sky-transparent-bg.jpg)] bg-cover bg-center-->