<script setup lang="ts">
import { site } from '~/data/site'
</script>

<template>
  <div class="grid gap-8 lg:grid-cols-[1fr_1.15fr] lg:items-stretch">
    <div class="space-y-4">
      <UiSectionTitle script="Canais de atendimento" title="Como podemos ajudar" />

      <div class="grid gap-4 pt-4 sm:grid-cols-2">
        <div class="border border-navy-800/10 bg-white p-6 shadow-sm">
          <span class="flex h-11 w-11 items-center justify-center rounded-full border border-gold-600/50 text-gold-600">
            <UiIcon name="phone" class="h-5 w-5" />
          </span>
          <h3 class="mt-4 text-xs font-semibold tracking-[0.2em] text-gold-700">TELEFONES</h3>
          <p v-for="p in site.phones" :key="p.href" class="mt-2 text-sm text-ink/80">
            <a :href="p.href" class="transition hover:text-gold-600">{{ p.label }}</a>
          </p>
        </div>

        <div class="border border-navy-800/10 bg-white p-6 shadow-sm">
          <span class="flex h-11 w-11 items-center justify-center rounded-full border border-gold-600/50 text-gold-600">
            <UiIcon name="mail" class="h-5 w-5" />
          </span>
          <h3 class="mt-4 text-xs font-semibold tracking-[0.2em] text-gold-700">E-MAIL</h3>
          <p v-for="e in site.emails" :key="e" class="mt-2 break-all text-sm text-ink/80">
            <a :href="`mailto:${e}`" class="transition hover:text-gold-600">{{ e }}</a>
          </p>
        </div>

        <div class="border border-navy-800/10 bg-white p-6 shadow-sm sm:col-span-2">
          <div class="flex items-start gap-4">
            <span class="flex h-11 w-11 shrink-0 items-center justify-center rounded-full border border-gold-600/50 text-gold-600">
              <UiIcon name="pin" class="h-5 w-5" />
            </span>
            <div>
              <h3 class="text-xs font-semibold tracking-[0.2em] text-gold-700">ENDEREÇO</h3>
              <address class="mt-2 text-sm not-italic leading-relaxed text-ink/80">
                {{ site.address.street }}<br>{{ site.address.district }} · CEP {{ site.address.cep }}<br>{{ site.address.city }}
              </address>
              <a :href="site.mapsUrl" target="_blank" rel="noopener" class="mt-3 inline-block text-xs font-semibold tracking-[0.2em] text-gold-700 transition hover:text-gold-600">
                COMO CHEGAR →
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="flex flex-wrap items-center gap-4 pt-2">
        <a :href="site.whatsapp" target="_blank" rel="noopener" class="bg-gold-600 px-8 py-3.5 text-xs font-semibold tracking-[0.2em] text-white transition hover:bg-gold-700">
          FALAR PELO WHATSAPP
        </a>
        <div class="flex gap-3">
          <a :href="site.instagram" target="_blank" rel="noopener" aria-label="Instagram" class="flex h-11 w-11 items-center justify-center rounded-full border border-navy-800/20 text-navy-800 transition hover:border-gold-600 hover:bg-gold-600 hover:text-white">
            <UiIcon name="instagram" class="h-5 w-5" />
          </a>
          <a :href="site.linkedin" target="_blank" rel="noopener" aria-label="LinkedIn" class="flex h-11 w-11 items-center justify-center rounded-full border border-navy-800/20 text-navy-800 transition hover:border-gold-600 hover:bg-gold-600 hover:text-white">
            <UiIcon name="linkedin" class="h-5 w-5" />
          </a>
        </div>
      </div>
    </div>

    <div class="relative min-h-[22rem] border border-navy-800/10 bg-white p-2 shadow-lg lg:min-h-[32rem]">
      <iframe
        :src="site.mapsEmbed"
        title="Mapa com a localização do escritório"
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
        class="absolute inset-2 h-[calc(100%-1rem)] w-[calc(100%-1rem)]"
      />
    </div>
  </div>
</template>
