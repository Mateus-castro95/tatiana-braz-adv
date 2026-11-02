<script setup lang="ts">
import { areas } from '~/data/areas'
</script>

<template>
  <section class="mx-auto max-w-7xl px-6 py-20 md:py-24">
    <div class="grid gap-6 md:grid-cols-2">
      <article v-for="(area, i) in areas" :key="area.title" class="border-l-2 border-gold-600 bg-white p-8 shadow-sm">
        <span class="text-xs font-semibold tracking-widest text-gold-600">{{ String(i + 1).padStart(2, '0') }}</span>
        <h2 class="mt-2 text-xl font-semibold text-navy-800">{{ area.title }}</h2>
        <p class="mt-3 text-sm leading-relaxed text-ink/75">{{ area.text }}</p>
      </article>
    </div>
  </section>
</template>
