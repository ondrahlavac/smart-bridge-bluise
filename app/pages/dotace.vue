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
import { MetaInfo } from 'vue-meta';

@Component({
  // Called to know which transition to apply
  transition(to, from) {
    if (!from) {
      return 'slide-left';
    }

    return 'slide-right';
  },

  head(): MetaInfo {
    return {
      title: this.page.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.page.seoDescription,
        },
        {
          hid: 'og:image',
          name: 'og:image',
          content: this.page.seoMetaImage,
        },
      ],
    };
  },
})
export default class Dotace extends Vue {
  page!: Page;

  async asyncData({ params, payload }): Promise<{ page: Page }> {
    console.log(`dostali jsme async page? -  ${params} `);
    if (payload) {
      return { page: payload };
    }
    try {
      const page = require(`@/content/pages/dotace.json`);

      return {
        page,
      };
    } catch (e) {
      throw new Error('Not found');
    }
  }
}
</script>
