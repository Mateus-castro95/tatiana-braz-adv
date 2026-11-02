<script setup lang="ts">
const items = [
  { icon: 'briefcase', title: 'Consultoria jurídica', text: 'Orientação preventiva e soluções claras para decisões seguras.' },
  { icon: 'scale', title: 'Atuação estratégica', text: 'Representação rigorosa, com estratégia única para cada demanda.' },
  { icon: 'target', title: 'Resultados concretos', text: 'Compromisso com os objetivos e o crescimento dos nossos Clientes.' }
]
</script>

<template>
  <section class="relative z-10 mx-auto -mt-16 max-w-6xl px-6">
    <div class="grid gap-5 md:grid-cols-3">
      <article v-for="item in items" :key="item.title" class="bg-white p-8 text-center shadow-xl">
        <span class="mx-auto flex h-12 w-12 items-center justify-center rounded-full bg-navy-800 text-gold-500">
          <UiIcon :name="item.icon" class="h-6 w-6" />
        </span>
        <h3 class="mt-5 text-xs font-semibold tracking-[0.2em] text-navy-800">{{ item.title.toUpperCase() }}</h3>
        <p class="mt-3 text-sm leading-relaxed text-ink/70">{{ item.text }}</p>
      </article>
    </div>
  </section>
</template>
