<script setup lang="ts">
// `script` = eyebrow em caixa-alta acima do título
defineProps<{
  script: string
  title: string
  text?: string
}>()
</script>

<template>
  <section class="bg-navy-800 text-white">
    <div class="mx-auto max-w-7xl px-6 py-20 md:py-28">
      <p class="text-xs font-semibold tracking-[0.3em] text-gold-500">{{ script.toUpperCase() }}</p>
      <h1 class="mt-3 text-4xl md:text-5xl">{{ title }}</h1>
      <span class="mt-6 block h-px w-14 bg-gold-600" />
      <p v-if="text" class="mt-6 max-w-2xl text-base leading-relaxed text-white/70">{{ text }}</p>
    </div>
  </section>
</template>
