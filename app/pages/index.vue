<template>
  <section class="home">
    <!-- Hero card -->
    <div class="relative">
      <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
        <div class="relative shadow-xl sm:rounded-2xl sm:overflow-hidden">
          <div class="absolute inset-0">
            <img class="h-full w-full object-cover" src="images/uploads/IoT-banner.png" alt="People working on laptops" />
            <div class="absolute inset-0 bg-indigo-700 mix-blend-multiply"></div>
          </div>
          <div class="relative px-4 py-16 sm:px-6 sm:py-24 lg:py-32 lg:px-8">
            <h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-5xl lg:text-6xl">
              <span class="block text-white">Jsme Smart Bridge</span>
              <span class="block text-indigo-200">váš poradce v oblasti IoT a technologií</span>
            </h1>
          </div>
        </div>
      </div>
    </div>

    <!-- More main page content here... -->

    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center">
      <div class="flex flex-col w-full xl:w-3/5 justify-center lg:items-start overflow-y-hidden">
        <div v-html="$md.render(welcomeText)" class="home__welcome markdown" />

        <div class="flex flex-col w-full xl:w-2/5">
          <img src="images/uploads/IoT-banner.png" class="rounded" alt="Městské panorama s ikonami možných IoT aplikací" />
        </div>

        <div class="flex flex-col w-full">
          <h2>Návrh projektů pro implementaci IoT</h2>
        </div>

        <div class="relative bg-white pt-16 pb-32 overflow-hidden">
          <div class="relative">
            <div class="lg:mx-auto lg:max-w-7xl lg:px-8 lg:grid lg:grid-cols-2 lg:grid-flow-col-dense lg:gap-24">
              <div class="px-4 max-w-xl mx-auto sm:px-6 lg:py-16 lg:max-w-none lg:mx-0 lg:px-0">
                <div>
                  <div>
                    <span class="h-12 w-12 rounded-md flex items-center justify-center bg-indigo-600">
                      <InboxIcon class="h-6 w-6 text-white" aria-hidden="true" />
                    </span>
                  </div>
                  <div class="mt-6">
                    <h2 class="text-3xl font-extrabold tracking-tight text-gray-900">Projektový management</h2>
                    <p class="mt-4 text-lg text-gray-500">
                      Semper curabitur ullamcorper posuere nunc sed. Ornare iaculis bibendum malesuada faucibus lacinia porttitor. Pulvinar
                      laoreet sagittis viverra duis. In venenatis sem arcu pretium pharetra at. Lectus viverra dui tellus ornare pharetra.
                    </p>
                    <div class="mt-6">
                      <a
                        href="#"
                        class="inline-flex px-4 py-2 border border-transparent text-base font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700"
                      >
                        Get started
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="mt-24">
            <div class="lg:mx-auto lg:max-w-7xl lg:px-8 lg:grid lg:grid-cols-2 lg:grid-flow-col-dense lg:gap-24">
              <div class="px-4 max-w-xl mx-auto sm:px-6 lg:py-32 lg:max-w-none lg:mx-0 lg:px-0 lg:col-start-2">
                <div>
                  <div>
                    <span class="h-12 w-12 rounded-md flex items-center justify-center bg-indigo-600">
                      <SparklesIcon class="h-6 w-6 text-white" aria-hidden="true" />
                    </span>
                  </div>
                  <div class="mt-6">
                    <h2 class="text-3xl font-extrabold tracking-tight text-gray-900">Dotace</h2>
                    <p class="mt-4 text-lg text-gray-500">
                      Semper curabitur ullamcorper posuere nunc sed. Ornare iaculis bibendum malesuada faucibus lacinia porttitor. Pulvinar
                      laoreet sagittis viverra duis. In venenatis sem arcu pretium pharetra at. Lectus viverra dui tellus ornare pharetra.
                    </p>
                    <div class="mt-6">
                      <a
                        href="#"
                        class="inline-flex px-4 py-2 border border-transparent text-base font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700"
                      >
                        Get started
                      </a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="mt-12 sm:mt-16 lg:mt-0 lg:col-start-1">
                <div class="pr-4 -ml-48 sm:pr-6 md:-ml-16 lg:px-0 lg:m-0 lg:relative lg:h-full">
                  <img
                    class="w-full rounded-xl shadow-xl ring-1 ring-black ring-opacity-5 lg:absolute lg:right-0 lg:h-full lg:w-auto lg:max-w-none"
                    src="https://tailwindui.com/img/component-images/inbox-app-screenshot-2.jpg"
                    alt="Customer profile user interface"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="flex flex-col w-full">
          <h2>Projektový management</h2>
        </div>

        <div class="flex flex-col w-full">
          <h2>Dotace</h2>
        </div>

        <div class="bg-gray-50 overflow-hidden">
          <div class="relative max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
            <div class="relative lg:grid lg:grid-cols-3 lg:gap-x-8">
              <div class="lg:col-span-1">
                <h2 class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-4xl">Poradenství v oblasti technologií</h2>
              </div>
              <dl class="mt-10 space-y-10 sm:space-y-0 sm:grid sm:grid-cols-2 sm:gap-x-8 sm:gap-y-10 lg:mt-0 lg:col-span-2">
                <div v-for="oblast in poradenskeOblasti" :key="oblast.name">
                  <dt>
                    <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                      <img class="h-6 w-6 text-white" aria-hidden="true" alt="icon" />
                    </div>
                    <p class="mt-5 text-lg leading-6 font-medium text-gray-900">{{ oblast.name }}</p>
                  </dt>
                  <dd class="mt-2 text-base text-gray-500">
                    {{ oblast.description }}
                  </dd>
                </div>
              </dl>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

const oblastiPoradenstvi = [
  { name: `Komunikační technologie a IoT`, description: `` },
  { name: `Industry 4.0`, description: `` },
  { name: `Regulace trhu elektronických komunikací`, description: `` },
  { name: `Energetika`, description: `Komunikační infrastruktura, AMM, Smart Metering` },
];

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
})
export default class Home extends Vue {
  welcomeText = settings.welcomeText;

  poradenskeOblasti = oblastiPoradenstvi;

  get posts(): Post[] {
    return this.$store.state.posts;
  }
}
</script>
