<template>
  <section class="page">
    <h1 class="page__title text-lg md:text-xl lg:text-4xl xl:text-6xl text-center py-8 md:py-16">Komplexní přístup k dotacím</h1>

    <div class="page__content markdown pt-4 md:pt-6 md:pb-24">
      Zaměřujeme se na celý proces dotačních možností, od designu projektových záměrů, přes vyhledání vhodného dotačního titulu, získání
      dotace až po konzultace s poskytovateli dotací pro nastavení podmínek dotačních titulů.
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component({
  // Called to know which transition to apply
  transition(to, from) {
    if (!from) {
      return 'slide-left';
    }

    return 'slide-right';
  },
})
export default class Dotace extends Vue {
  page!: Page;

  async asyncData({ params, payload }): Promise<{ page: Page }> {
    console.log(`sfd -  ${params.page} `);
    if (payload) {
      return { page: payload };
    }
    return { page: payload };
  }
}
</script>
