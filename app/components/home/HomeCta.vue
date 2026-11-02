<script setup lang="ts">
import { site } from '~/data/site'
</script>

<template>
  <section class="bg-navy-900 text-white">
    <div class="mx-auto flex max-w-7xl flex-col items-start justify-between gap-6 px-6 py-16 md:flex-row md:items-center">
      <div>
        <h2 class="text-3xl">Vamos conversar?</h2>
        <p class="mt-2 max-w-lg text-sm text-white/65">Cada demanda merece uma estratégia única. Fale com a Dra. Tatiana.</p>
      </div>
      <a :href="site.whatsapp" target="_blank" rel="noopener" class="bg-gold-600 px-8 py-3 text-xs font-semibold tracking-[0.2em] transition hover:bg-gold-700">
        CHAMAR NO WHATSAPP
      </a>
    </div>
  </section>
</template>
