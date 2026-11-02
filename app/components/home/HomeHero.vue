<script setup lang="ts">
import { site } from '~/data/site'
</script>

<template>
  <section class="bg-navy-800 text-white">
    <div class="mx-auto grid max-w-7xl items-center px-6 pt-16 md:grid-cols-2 md:gap-10 md:pt-0">
      <div class="md:py-32">
        <p class="text-xs font-semibold tracking-[0.3em] text-gold-500">ADVOGADOS AO SEU LADO</p>
        <h1 class="mt-5 text-4xl leading-tight md:text-5xl">
          Construindo relações de <span class="text-gold-500">confiança</span>
        </h1>
        <span class="mt-6 block h-px w-14 bg-gold-600" />
        <p class="mt-6 max-w-md leading-relaxed text-white/70">
          Assessoria jurídica estratégica, moderna e personalizada, para proteger seus interesses e defender seus direitos.
        </p>
        <div class="mt-9 hidden flex-wrap gap-4 md:flex">
          <NuxtLink to="/areas-de-atuacao" class="bg-gold-600 px-7 py-3 text-xs font-semibold tracking-[0.2em] transition hover:bg-gold-700">
            NOSSAS ÁREAS
          </NuxtLink>
          <a :href="site.whatsapp" target="_blank" rel="noopener" class="border border-gold-600 px-7 py-3 text-xs font-semibold tracking-[0.2em] transition hover:bg-gold-600">
            FALE CONOSCO
          </a>
        </div>
      </div>
      <div class="relative -mt-4 h-[26rem] sm:h-[30rem] md:mt-0 md:h-[36rem]">
        <img
          src="/tatiana-hero.webp"
          alt="Tatiana Braz Lux, advogada"
          class="hero-photo mx-auto h-full w-auto md:w-full md:object-cover md:object-[60%_25%]"
          fetchpriority="high"
        >
      </div>
      <div class="-mt-2 grid grid-cols-2 gap-3 pb-28 md:hidden">
        <NuxtLink to="/areas-de-atuacao" class="bg-gold-600 px-3 py-3 text-center text-[0.65rem] font-semibold tracking-[0.15em] transition hover:bg-gold-700">
          NOSSAS ÁREAS
        </NuxtLink>
        <a :href="site.whatsapp" target="_blank" rel="noopener" class="border border-gold-600 px-3 py-3 text-center text-[0.65rem] font-semibold tracking-[0.15em] transition hover:bg-gold-600">
          FALE CONOSCO
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Dissolve as bordas da foto no fundo da seção, sem recorte visível */
.hero-photo {
  --fade-x: linear-gradient(to right, transparent 0%, #000 28%, #000 88%, transparent 100%);
  --fade-y: linear-gradient(to bottom, transparent 0%, #000 18%, #000 78%, transparent 100%);
  -webkit-mask-image: var(--fade-x), var(--fade-y);
  -webkit-mask-composite: source-in;
  mask-image: var(--fade-x), var(--fade-y);
  mask-composite: intersect;
}
</style>
