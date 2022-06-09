<template>
  <section class="page">
    <div class="py-12 bg-white">
      <div class="max-w-7xl mx-auto px-4 space-y-8 sm:px-6 lg:px-8">
        <div class="lg:text-center">
          <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">IoT</h2>
          <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">Internet věcí</p>
          <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
            Internet věcí neboli „Internet of Things“ („IoT“) je v současnosti tématem, které hýbe technologickým světem.
          </p>
        </div>
        <div class="relative z-10">
          <div class="prose prose-indigo text-gray-500 mx-auto lg:max-w-none" style="line-height: 1.75">
            <p style="margin-top: 1.25em; margin-bottom: 1.25em">
              Rychlý rozvoj bezdrátových technologií v posledních letech přinesl diametrální nárůst počtu inteligentních zařízení
              připojených k internetu.
            </p>
            <p style="margin-top: 1.25em; margin-bottom: 1.25em">
              Fenomén internetu věcí pak umožňuje nejen sbírat z míst dosud nedostupných (např. z míst bez stálého zdroje elektřiny nebo
              díky nízké ceně senzorů i z míst, kde to bylo dosud finančně nemožné), lokálně vyhodnocovat získaná data a nastavit základní
              reakce a upozornění, ale i vzdáleně ovládat zařízení a na základě centrální analýzy dat i predikovat chování, vytvářet modely
              z různých vstupních dat a hlavně vzdáleně zpřístupnit získaná data pomocí mobilních nebo internetových aplikací.
            </p>
            <p style="margin-top: 1.25em; margin-bottom: 1.25em">
              K dispozici je tak nově i velké množství dat z těchto zařízení. Ta v kombinaci s pokročilými možnostmi analýzy umožňují nové
              aplikace například v oblastech zabezpečení, sledování nebo měření.
            </p>
            <h3 style="color: black; font-weight: 600; font-size: 1.25em; margin-top: 1.6em; margin-bottom: 0.6em; line-height: 1.6">
              Jsme tu pro Vás
            </h3>
            <p style="margin-top: 1.25em; margin-bottom: 1.25em">
              Společnost Smart Bridge zajišťuje komplexní služby v oblasti internetu věcí - od zajištění hardwaru pro sběr dat až po vývoj a
              poskytnutí mobilních a internetových aplikací vytvořených pro potřebu dané služby a klienta včetně následného dohledu a
              zákaznické péče.
            </p>
          </div>
          <div class="mt-10 flex text-base max-w-prose mx-auto lg:max-w-none">
            <div class="rounded-md shadow">
              <a
                href="/kontakt"
                class="w-full flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700"
              >
                Kontaktujte nás
              </a>
            </div>
            <!--            <div class="rounded-md shadow ml-4">-->
            <!--              <a-->
            <!--                href="#"-->
            <!--                class="w-full flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-indigo-600 bg-white hover:bg-gray-50"-->
            <!--              >-->
            <!--                Learn more-->
            <!--              </a>-->
            <!--            </div>-->
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import { MetaInfo } from 'vue-meta';

@Component({
  transition(to, from) {
    if (!from) {
      return 'slide-left';
    }
    return 'slide-right';
  },

  head(): MetaInfo {
    return {
      title: 'Internet věcí',
      meta: [
        { hid: 'description', name: 'description', content: 'IoT - Internet of Things neboli internet věcí.' },
        { hid: 'og:image', name: 'og:image', content: '/empty.png' },
      ],
    };
  },
})
export default class InternetOfThings extends Vue {}
</script>
