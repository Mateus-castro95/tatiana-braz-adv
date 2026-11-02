<script setup lang="ts">
// Troque o `src` quando as fotos profissionais forem entregues.
defineProps<{ src?: string, alt?: string, label?: string, imgClass?: string }>()
</script>

<template>
  <div class="relative overflow-hidden bg-gradient-to-br from-navy-600 to-navy-900">
    <img v-if="src" :src="src" :alt="alt ?? ''" class="absolute inset-0 h-full w-full object-cover" :class="imgClass">
    <span v-else class="absolute inset-0 flex items-center justify-center px-4 text-center text-xs tracking-[0.3em] text-gold-500/70">
      {{ (label ?? 'FOTO').toUpperCase() }}
    </span>
  </div>
</template>
