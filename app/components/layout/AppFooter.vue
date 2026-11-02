<script setup lang="ts">
import { site } from '~/data/site'
</script>

<template>
  <footer class="bg-navy-900 text-white/80">
    <div class="mx-auto grid max-w-7xl gap-10 px-6 py-14 md:grid-cols-[1fr_1fr_1.2fr]">
      <div>
        <div class="flex items-center gap-4">
          <img src="/icone-b.png" alt="" class="h-14 w-auto" width="32" height="56">
          <div>
            <p class="text-xl font-semibold tracking-[0.2em] text-white">TATIANA BRAZ</p>
            <p class="text-[0.6rem] tracking-[0.35em] text-gold-300">ADVOGADA</p>
          </div>
        </div>
        <p class="mt-5 max-w-xs text-sm leading-relaxed">
          Assessoria jurídica estratégica, moderna e personalizada, com atuação nacional a partir de Jaraguá do Sul/SC.
        </p>
        <div class="mt-6 flex gap-3">
          <a :href="site.instagram" target="_blank" rel="noopener" aria-label="Instagram" class="flex h-10 w-10 items-center justify-center rounded-full border border-white/20 text-white/80 transition hover:border-gold-500 hover:bg-gold-600 hover:text-white">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class="h-[1.1rem] w-[1.1rem]" aria-hidden="true">
              <rect x="3" y="3" width="18" height="18" rx="5" />
              <circle cx="12" cy="12" r="4" />
              <circle cx="17.5" cy="6.5" r="0.6" fill="currentColor" />
            </svg>
          </a>
          <a :href="site.linkedin" target="_blank" rel="noopener" aria-label="LinkedIn" class="flex h-10 w-10 items-center justify-center rounded-full border border-white/20 text-white/80 transition hover:border-gold-500 hover:bg-gold-600 hover:text-white">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class="h-[1.1rem] w-[1.1rem]" aria-hidden="true">
              <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-4 0v7h-4v-7a6 6 0 0 1 6-6z" />
              <rect x="2" y="9" width="4" height="12" />
              <circle cx="4" cy="4" r="2" />
            </svg>
          </a>
        </div>
      </div>

      <div>
        <h3 class="mb-4 text-sm font-semibold tracking-widest text-gold-500">CONTATO</h3>
        <ul class="space-y-2 text-sm">
          <li v-for="p in site.phones" :key="p.href"><a :href="p.href" class="hover:text-gold-500">{{ p.label }}</a></li>
          <li v-for="e in site.emails" :key="e"><a :href="`mailto:${e}`" class="break-all hover:text-gold-500">{{ e }}</a></li>
        </ul>
      </div>

      <div>
        <h3 class="mb-4 text-sm font-semibold tracking-widest text-gold-500">LOCALIZAÇÃO</h3>
        <address class="text-sm not-italic leading-relaxed">
          {{ site.address.street }}<br>{{ site.address.district }} · CEP {{ site.address.cep }}<br>{{ site.address.city }}
        </address>
        <a :href="site.mapsUrl" target="_blank" rel="noopener" class="group mt-5 block overflow-hidden border border-white/10 transition hover:border-gold-500" aria-label="Abrir endereço no Google Maps">
          <iframe
            :src="site.mapsEmbed"
            title="Mapa com a localização do escritório"
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            class="pointer-events-none h-40 w-full opacity-90 grayscale transition group-hover:grayscale-0"
          />
        </a>
      </div>
    </div>
    <div class="border-t border-white/10 py-5 text-center text-xs text-white/50">
      © {{ new Date().getFullYear() }} {{ site.fullName }}. Todos os direitos reservados.
    </div>
  </footer>
</template>
