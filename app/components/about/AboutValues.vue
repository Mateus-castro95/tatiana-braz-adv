<script setup lang="ts">
import { values } from '~/data/areas'
</script>

<template>
  <section class="mx-auto max-w-7xl px-6 py-20 md:py-24">
    <UiSectionTitle script="O que nos guia" title="Nossos Valores" center />
    <ul class="mt-12 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
      <li v-for="v in values" :key="v" class="border border-gold-300 bg-white px-6 py-5 text-center text-sm font-semibold tracking-widest text-navy-800">
        {{ v.toUpperCase() }}
      </li>
    </ul>
  </section>
</template>
