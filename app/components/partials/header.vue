<template>
  <section>
    <header>
      <Popover class="relative bg-white">
        <div class="flex justify-between items-center max-w-7xl mx-auto px-4 py-6 sm:px-6 md:justify-start md:space-x-10 lg:px-8">
          <div class="flex justify-start lg:w-0 lg:flex-1">
            <nuxt-link to="/">
              <span class="sr-only">Smart Bridge</span>
              <img class="h-8 w-auto sm:h-10" :src="logo" alt="SmartBridge" />
            </nuxt-link>
          </div>
          <div class="-mr-2 -my-2 md:hidden">
            <PopoverButton
              class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
            >
              <span class="sr-only">Open menu</span>
              <MenuIcon class="h-6 w-6" aria-hidden="true" />
            </PopoverButton>
          </div>
          <PopoverGroup as="nav" class="hidden md:flex space-x-10">
            <nuxt-link to="/o-nas" class="text-base font-medium text-gray-500 hover:text-gray-900"> O nás </nuxt-link>
            <nuxt-link to="/iot" class="text-base font-medium text-gray-500 hover:text-gray-900"> Internet of Things </nuxt-link>
            <nuxt-link to="/dotace" class="text-base font-medium text-gray-500 hover:text-gray-900"> Dotace </nuxt-link>
          </PopoverGroup>
          <div class="hidden md:flex items-center justify-end md:flex-1 lg:w-0">
            <nuxt-link
              to="/kontakt"
              class="ml-8 whitespace-nowrap inline-flex items-center justify-center bg-gradient-to-r from-purple-600 to-indigo-600 bg-origin-border px-4 py-2 border border-transparent rounded-md shadow-sm text-base font-medium text-white hover:from-purple-700 hover:to-indigo-700"
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
          <PopoverPanel focus class="absolute z-30 top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden">
            <div class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y-2 divide-gray-50">
              <div class="pt-5 pb-6 px-5">
                <div class="flex items-center justify-between">
                  <div>
                    <img
                      class="h-8 w-auto"
                      src="https://tailwindui.com/img/logos/workflow-mark-purple-600-to-indigo-600.svg"
                      alt="Workflow"
                    />
                  </div>
                  <div class="-mr-2">
                    <PopoverButton
                      class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                    >
                      <span class="sr-only">Close menu</span>
                      <XIcon class="h-6 w-6" aria-hidden="true" />
                    </PopoverButton>
                  </div>
                </div>
              </div>
              <div class="py-6 px-5">
                <div class="grid grid-cols-2 gap-4">
                  <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700"> Pricing </a>
                  <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700"> Partners </a>
                  <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700"> Company </a>
                </div>
                <div class="mt-6">
                  <a
                    href="#"
                    class="w-full flex items-center justify-center bg-gradient-to-r from-purple-600 to-indigo-600 bg-origin-border px-4 py-2 border border-transparent rounded-md shadow-sm text-base font-medium text-white hover:from-purple-700 hover:to-indigo-700"
                  >
                    Sign up
                  </a>
                  <p class="mt-6 text-center text-base font-medium text-gray-500">
                    Existing customer?
                    <a href="#" class="text-gray-900"> Sign in </a>
                  </p>
                </div>
              </div>
            </div>
          </PopoverPanel>
        </transition>
      </Popover>
    </header>
    <!--    <header class="flex items-center py-4 md:py-8">-->
    <!--      <div class="header__logo">-->
    <!--        <nuxt-link to="/">-->
    <!--          <img :src="logo" alt="Logo" class="w-40" />-->
    <!--        </nuxt-link>-->
    <!--      </div>-->

    <!--      <nav class="nav ml-auto">-->
    <!--        <ul class="flex flex-row items-center sm:mt-4 sm:pt-4 md:mt-0 md:pt-0 md:mr-4 lg:mr-8">-->
    <!--          &lt;!&ndash;        <li>&ndash;&gt;-->
    <!--          &lt;!&ndash;          <nuxt-link to="/blog" class="block font-medium px-4 py-1 md:p-2 lg:px-4">&ndash;&gt;-->
    <!--          &lt;!&ndash;            Blog&ndash;&gt;-->
    <!--          &lt;!&ndash;          </nuxt-link>&ndash;&gt;-->
    <!--          &lt;!&ndash;        </li>&ndash;&gt;-->
    <!--          <li v-for="(page, index) in pages" :key="index" class="block font-medium px-4 py-1 md:p-2 lg:px-4">-->
    <!--            <nuxt-link :to="`/${page.slug}`">{{ page.title }}</nuxt-link>-->
    <!--          </li>-->
    <!--        </ul>-->
    <!--      </nav>-->
    <!--    </header>-->
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
}
</script>

<style lang="scss">
.nav {
  ul li > a {
    &.nuxt-link-active {
      color: $bluise;
      @apply font-bold;
    }
  }
}
</style>
