<template>
  <section>
    <header>
      <div class="relative bg-white">
        <div class="flex justify-between items-center max-w-7xl mx-auto px-4 py-6 sm:px-6 md:justify-start md:space-x-10">
          <div class="flex justify-start lg:w-0 lg:flex-1">
            <nuxt-link to="/">
              <span class="sr-only">Smart Bridge</span>
              <img class="h-8 w-auto sm:h-10" :src="logo" alt="SmartBridge" />
            </nuxt-link>
          </div>
          <div class="-mr-2 -my-2 md:hidden">
            <div
              @click="mobileMenuShow = true"
              @keydown.enter="mobileMenuShow = true"
              class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
            >
              <span class="sr-only">Otevřít nabídku</span>
              <svg
                class="h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="2"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"></path>
              </svg>
            </div>
          </div>
          <div class="hidden md:flex space-x-10">
            <nuxt-link to="/" class="text-base font-medium text-gray-500 hover:text-gray-900"> O nás </nuxt-link>
            <nuxt-link to="/iot" class="text-base font-medium text-gray-500 hover:text-gray-900"> Internet of Things </nuxt-link>
            <nuxt-link to="/dotace" class="text-base font-medium text-gray-500 hover:text-gray-900"> Dotace </nuxt-link>
          </div>
          <div class="hidden md:flex items-center justify-end md:flex-1 lg:w-0">
            <nuxt-link
              to="/kontakt"
              class="ml-8 whitespace-nowrap inline-flex items-center justify-center px-4 py-2 border border-transparent rounded-md shadow-sm text-base font-medium text-white bg-indigo-600 hover:bg-indigo-700"
              >Kontakt
            </nuxt-link>
          </div>
        </div>

        <transition
          enter-active-class="duration-200 ease-out"
          enter-from-class="opacity-0 scale-95"
          enter-to-class="opacity-100 scale-100"
          leave-active-class="duration-100 ease-in"
          leave-from-class="opacity-100 scale-100"
          leave-to-class="opacity-0 scale-95"
        >
          <div
            v-if="mobileMenuShow"
            class="absolute top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden"
            style="z-index: 100"
          >
            <div class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y-2 divide-gray-50">
              <div class="pt-5 pb-6 px-5">
                <div class="flex items-center justify-between">
                  <div>
                    <img class="h-8 w-auto" :src="logo" alt="SmartBridge" />
                  </div>
                  <div class="-mr-2">
                    <button
                      @click="mobileMenuShow = false"
                      @keydown.esc="mobileMenuShow = false"
                      class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                    >
                      <span class="sr-only">Close menu</span>
                      <svg
                        class="h-6 w-6"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="2"
                        stroke="currentColor"
                        aria-hidden="true"
                      >
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"></path>
                      </svg>
                    </button>
                  </div>
                </div>
                <div class="mt-6">
                  <nav class="grid grid-cols-1 gap-7">
                    <nuxt-link to="/" @click="mobileMenuShow = false" class="-m-3 p-3 flex items-center rounded-lg hover:bg-gray-50">
                      <div class="flex-shrink-0 flex items-center justify-center h-10 w-10 rounded-md bg-indigo-500 text-white">
                        <svg
                          class="h-6 w-6"
                          xmlns="http://www.w3.org/2000/svg"
                          fill="none"
                          viewBox="0 0 24 24"
                          stroke-width="2"
                          stroke="currentColor"
                          aria-hidden="true"
                        >
                          <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
                          />
                        </svg>
                      </div>
                      <div class="ml-4 text-base font-medium text-gray-900">O nás</div>
                    </nuxt-link>
                    <nuxt-link to="/iot" @click="mobileMenuShow = false" class="-m-3 p-3 flex items-center rounded-lg hover:bg-gray-50">
                      <div class="flex-shrink-0 flex items-center justify-center h-10 w-10 rounded-md bg-indigo-500 text-white">
                        <svg
                          class="h-6 w-6"
                          xmlns="http://www.w3.org/2000/svg"
                          fill="none"
                          viewBox="0 0 24 24"
                          stroke-width="2"
                          stroke="currentColor"
                          aria-hidden="true"
                        >
                          <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M8.684 13.342C8.886 12.938 9 12.482 9 12c0-.482-.114-.938-.316-1.342m0 2.684a3 3 0 110-2.684m0 2.684l6.632 3.316m-6.632-6l6.632-3.316m0 0a3 3 0 105.367-2.684 3 3 0 00-5.367 2.684zm0 9.316a3 3 0 105.368 2.684 3 3 0 00-5.368-2.684z"
                          />
                        </svg>
                      </div>
                      <div class="ml-4 text-base font-medium text-gray-900">Internet of Things</div>
                    </nuxt-link>
                    <nuxt-link to="/dotace" @click="mobileMenuShow = false" class="-m-3 p-3 flex items-center rounded-lg hover:bg-gray-50">
                      <div class="flex-shrink-0 flex items-center justify-center h-10 w-10 rounded-md bg-indigo-500 text-white">
                        <svg
                          class="h-6 w-6"
                          xmlns="http://www.w3.org/2000/svg"
                          fill="none"
                          viewBox="0 0 24 24"
                          stroke-width="2"
                          stroke="currentColor"
                          aria-hidden="true"
                        >
                          <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M14.121 15.536c-1.171 1.952-3.07 1.952-4.242 0-1.172-1.953-1.172-5.119 0-7.072 1.171-1.952 3.07-1.952 4.242 0M8 10.5h4m-4 3h4m9-1.5a9 9 0 11-18 0 9 9 0 0118 0z"
                          />
                        </svg>
                      </div>
                      <div class="ml-4 text-base font-medium text-gray-900">Dotace</div>
                    </nuxt-link>
                  </nav>
                </div>
              </div>
              <div class="py-6 px-5">
                <div class="mt-6" @click="showMobileMenu = false" @keydown.enter="window.alert('hide plz')">
                  <nuxt-link
                    to="/kontakt"
                    class="w-full flex items-center justify-center px-4 py-2 border border-transparent rounded-md shadow-sm text-base font-medium text-white bg-indigo-600 hover:bg-indigo-700"
                  >
                    Kontakt
                  </nuxt-link>
                </div>
              </div>
            </div>
          </div>
        </transition>
      </div>
    </header>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component
export default class Header extends Vue {
  get pages(): Page[] {
    return this.$store.state.pages;
  }

  logo = settings.logo;

  mobileMenuShow = false;
}
</script>
