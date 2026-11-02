<script setup lang="ts">
import { navLinks, site } from '~/data/site'

const open = ref(false)
const route = useRoute()
watch(() => route.fullPath, () => (open.value = false))
</script>

<template>
  <header class="sticky top-0 z-40 bg-cream/95 text-navy-800 shadow-sm backdrop-blur">
    <div class="mx-auto flex max-w-7xl items-center justify-between px-6 py-4">
      <NuxtLink to="/" class="flex items-center gap-3 leading-none">
        <img src="/icone-b.png" alt="" class="h-10 w-auto" width="23" height="40">
        <span>
          <span class="block font-serif text-lg font-semibold tracking-[0.18em]">TATIANA BRAZ</span>
        <span class="block text-[0.55rem] tracking-[0.35em] text-gold-700">ADVOGADA</span>
        </span>
      </NuxtLink>

      <nav class="hidden items-center gap-9 md:flex">
        <NuxtLink
          v-for="link in navLinks"
          :key="link.to"
          :to="link.to"
          class="text-[0.7rem] font-medium tracking-[0.2em] transition hover:text-gold-600"
          active-class="text-gold-600"
        >
          {{ link.label.toUpperCase() }}
        </NuxtLink>
      </nav>

      <a :href="site.whatsapp" target="_blank" rel="noopener" class="hidden bg-gold-600 px-5 py-2.5 text-[0.7rem] font-semibold tracking-[0.2em] text-white transition hover:bg-gold-700 md:block">
        FALE CONOSCO
      </a>

      <button class="md:hidden" aria-label="Abrir menu" @click="open = !open">
        <span class="block h-0.5 w-6 bg-navy-800" />
        <span class="mt-1.5 block h-0.5 w-6 bg-navy-800" />
        <span class="mt-1.5 block h-0.5 w-6 bg-navy-800" />
      </button>
    </div>

    <nav v-if="open" class="flex flex-col items-end gap-4 border-t border-navy-800/10 px-6 py-5 md:hidden">
      <NuxtLink v-for="link in navLinks" :key="link.to" :to="link.to" class="text-xs tracking-[0.2em]" active-class="text-gold-600">
        {{ link.label.toUpperCase() }}
      </NuxtLink>
      <a :href="site.whatsapp" target="_blank" rel="noopener" class="bg-gold-600 px-5 py-2.5 text-xs font-semibold tracking-[0.2em] text-white">FALE CONOSCO</a>
    </nav>
  </header>
</template>
