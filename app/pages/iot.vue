<template>
  <div>
    <p>Internet věcí neboli „Internet of Things“ („IoT“) je v současnosti tématem, které hýbe technologickým světem.</p>
    <p>
      Rychlý rozvoj bezdrátových technologií v posledních letech přinesl diametrální nárůst počtu inteligentních zařízení připojených k
      internetu.
    </p>
    <p>
      K dispozici je tak nově i velké množství dat z těchto zařízení. Ta v kombinaci s pokročilými možnostmi analýzy umožňují nové aplikace
      například v oblastech zabezpečení, sledování nebo měření.
    </p>
    <p>
      Fenomén internetu věcí pak umožňuje nejen sbírat z míst dosud nedostupných (např. z míst bez stálého zdroje elektřiny nebo díky nízké
      ceně senzorů i z míst, kde to bylo dosud finančně nemožné), lokálně vyhodnocovat získaná data a nastavit základní reakce a upozornění,
      ale i vzdáleně ovládat zařízení a na základě centrální analýzy dat i predikovat chování, vytvářet modely z různých vstupních dat a
      hlavně vzdáleně zpřístupnit získaná data pomocí mobilních nebo internetových aplikací.
    </p>
    <p>
      Společnost Smart Bridge zajišťuje komplexní služby v oblasti internetu věcí - od zajištění hardwaru pro sběr dat až po vývoj a
      poskytnutí mobilních a internetových aplikací vytvořených pro potřebu dané služby a klienta včetně následného dohledu a zákaznické
      péče.
    </p>
  </div>
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
