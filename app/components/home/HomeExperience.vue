<script setup lang="ts">
const pillars = [
  { icon: 'shield', title: 'Estratégia', text: 'Soluções jurídicas pensadas sob medida para cada Cliente.' },
  { icon: 'users', title: 'Compromisso', text: 'Atendimento dedicado, ético e transparente.' },
  { icon: 'target', title: 'Performance', text: 'Foco em soluções eficazes e duradouras.' }
]
</script>

<template>
  <section class="bg-white">
    <div class="mx-auto grid max-w-7xl items-center gap-12 px-6 py-24 md:grid-cols-2">
      <div>
        <p class="mb-3 text-xs font-semibold tracking-[0.25em] text-gold-600">NOSSA EXPERIÊNCIA A SEU SERVIÇO</p>
        <h2 class="text-4xl leading-tight text-navy-800 md:text-5xl">
          Experiência.<br><span class="text-gold-600">Integridade. Resultados.</span>
        </h2>
        <p class="mt-6 max-w-md text-sm leading-relaxed text-ink/70">
          Com sede em Jaraguá do Sul/SC e atuação nacional, o escritório une experiência e uma abordagem humana para defender seus interesses.
        </p>
        <div class="mt-10 grid grid-cols-3 gap-4 text-center">
          <div v-for="p in pillars" :key="p.title">
            <span class="mx-auto flex h-16 w-16 items-center justify-center rounded-full border border-gold-500 text-gold-600">
              <UiIcon :name="p.icon" class="h-7 w-7" />
            </span>
            <h3 class="mt-4 text-[0.65rem] font-semibold tracking-[0.2em] text-navy-800">{{ p.title.toUpperCase() }}</h3>
            <p class="mt-2 text-xs leading-relaxed text-ink/60">{{ p.text }}</p>
          </div>
        </div>
      </div>
      <div class="relative h-[32rem] overflow-hidden bg-navy-900 md:h-[36rem]">
        <!-- Cópia desfocada da própria foto preenche as laterais -->
        <img src="/tatiana-final.webp" alt="" aria-hidden="true" class="absolute inset-0 h-full w-full scale-125 object-cover opacity-70 blur-2xl">
        <img
          src="/tatiana-final.webp"
          alt="Tatiana Braz Lux, advogada"
          class="relative mx-auto h-full w-auto max-w-full object-contain [mask-image:linear-gradient(to_right,transparent,#000_14%,#000_86%,transparent)]"
          loading="lazy"
        >
      </div>
    </div>
  </section>
</template>
