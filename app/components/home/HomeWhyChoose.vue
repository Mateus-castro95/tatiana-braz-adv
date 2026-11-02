<script setup lang="ts">
import { differentials } from '~/data/areas'
</script>

<template>
  <section class="mx-auto grid max-w-7xl items-center gap-14 px-6 py-24 md:grid-cols-2">
    <div>
      <UiSectionTitle script="Por que nos escolher" title="Comprometidos com o seu sucesso" />
      <p class="mt-6 max-w-lg text-sm leading-relaxed text-ink/70">
        Mais de 15 anos de experiência no Direito Corporativo, com ética, excelência e dedicação integral a cada Cliente.
      </p>
      <div class="mt-10 grid gap-x-8 gap-y-8 sm:grid-cols-2">
        <div v-for="item in differentials" :key="item.title" class="flex gap-4">
          <span class="flex h-10 w-10 shrink-0 items-center justify-center bg-gold-100 text-gold-700">
            <UiIcon :name="item.icon" class="h-5 w-5" />
          </span>
          <div>
            <h3 class="text-xs font-semibold tracking-wider text-navy-800">{{ item.title }}</h3>
            <p class="mt-1 text-xs leading-relaxed text-ink/60">{{ item.text }}</p>
          </div>
        </div>
      </div>
    </div>

    <div class="relative pb-16">
      <UiPhotoPlaceholder src="/escritorio.webp" img-class="object-[50%_18%]" alt="Escritório Tatiana Braz Advogada" label="Foto do escritório" class="h-96 w-full md:h-[28rem]" />
      <blockquote class="absolute bottom-0 left-6 right-6 bg-navy-800 p-7 text-white shadow-xl md:left-10 md:right-auto md:w-80">
        <span class="font-serif text-4xl leading-none text-gold-500">“</span>
        <p class="text-sm leading-relaxed text-white/85">
          Cada demanda merece uma estratégia única, construída com base na confiança, ética e resultados.
        </p>
      </blockquote>
    </div>
  </section>
</template>
