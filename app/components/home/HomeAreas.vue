<script setup lang="ts">
import { areas } from '~/data/areas'
</script>

<template>
  <section class="relative overflow-hidden bg-navy-800 py-24 text-white">
    <!-- brilho dourado sutil ao fundo -->
    <div class="pointer-events-none absolute -right-40 -top-40 h-[28rem] w-[28rem] rounded-full bg-gold-600/10 blur-3xl" />
    <div class="pointer-events-none absolute -bottom-48 -left-40 h-[28rem] w-[28rem] rounded-full bg-navy-500/20 blur-3xl" />

    <div class="relative mx-auto max-w-7xl px-6">
      <div class="flex flex-col gap-6 md:flex-row md:items-end md:justify-between">
        <UiSectionTitle script="Especialidades" title="Áreas de Atuação" light />
        <p class="max-w-sm text-sm leading-relaxed text-white/60">
          Atuação estratégica e personalizada em oito frentes do Direito, para pessoas e empresas.
        </p>
      </div>

      <div class="mt-14 grid gap-5 sm:grid-cols-2 lg:grid-cols-4">
        <NuxtLink
          v-for="(area, i) in areas"
          :key="area.title"
          to="/areas-de-atuacao"
          class="group relative flex flex-col overflow-hidden border border-white/10 bg-navy-700/60 p-7 transition duration-300 hover:-translate-y-1 hover:border-gold-600/60 hover:bg-navy-700"
        >
          <span class="absolute inset-x-0 top-0 h-0.5 origin-left scale-x-0 bg-gold-600 transition-transform duration-500 group-hover:scale-x-100" />
          <span class="absolute right-5 top-4 font-serif text-4xl text-white/[0.06] transition group-hover:text-gold-500/20">
            {{ String(i + 1).padStart(2, '0') }}
          </span>

          <span class="flex h-12 w-12 items-center justify-center rounded-full border border-gold-600/50 text-gold-500 transition group-hover:bg-gold-600 group-hover:text-white">
            <UiIcon :name="area.icon" class="h-5 w-5" />
          </span>

          <h3 class="mt-6 text-xs font-semibold tracking-[0.2em] text-gold-500">{{ area.title.toUpperCase() }}</h3>
          <p class="mt-3 line-clamp-4 text-sm leading-relaxed text-white/60">{{ area.text }}</p>

          <span class="mt-6 inline-flex items-center gap-2 pt-1 text-[0.65rem] font-semibold tracking-[0.2em] text-white/40 transition group-hover:text-gold-500">
            SAIBA MAIS <span class="transition-transform group-hover:translate-x-1">→</span>
          </span>
        </NuxtLink>
      </div>

      <div class="mt-12 flex justify-center">
        <NuxtLink to="/areas-de-atuacao" class="border border-gold-600 px-8 py-3 text-xs font-semibold tracking-[0.2em] text-gold-500 transition hover:bg-gold-600 hover:text-white">
          VER DETALHES DE CADA ÁREA
        </NuxtLink>
      </div>
    </div>
  </section>
</template>
