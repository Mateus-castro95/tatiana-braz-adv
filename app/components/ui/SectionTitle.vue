<script setup lang="ts">
// `script` = texto pequeno em caixa-alta acima do título (eyebrow)
defineProps<{
  script?: string
  title: string
  light?: boolean
  center?: boolean
}>()
</script>

<template>
  <div :class="center ? 'text-center' : ''">
    <p v-if="script" class="mb-3 text-xs font-semibold tracking-[0.25em] text-gold-600">{{ script.toUpperCase() }}</p>
    <h2 class="text-3xl leading-tight md:text-4xl" :class="light ? 'text-white' : 'text-navy-800'">
      {{ title }}
    </h2>
    <span class="mt-5 inline-block h-px w-14 bg-gold-600" />
  </div>
</template>
