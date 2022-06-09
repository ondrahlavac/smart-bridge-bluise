<template>
  <section class="page">
    <div class="py-12 bg-white">
      <div class="relative bg-white">
        <div class="absolute inset-0">
          <div class="absolute inset-y-0 left-0 w-1/2 bg-gray-50" />
        </div>
        <div class="relative max-w-7xl mx-auto lg:grid lg:grid-cols-5">
          <div class="bg-gray-50 py-16 px-4 sm:px-6 lg:col-span-2 lg:px-8 lg:py-24 xl:pr-12">
            <div class="max-w-lg mx-auto">
              <h2 class="text-2xl font-extrabold tracking-tight text-gray-900 sm:text-3xl">Neváhejte nás kontaktovat</h2>
              <p class="mt-3 text-lg leading-6 text-gray-500">
                SmartBridge je Váš poradce v oblasti IoT, projektového managementu a dotací. Zeptejte se nás, jak můžeme pomoci právě Vám.
              </p>
              <dl class="mt-8 text-base text-gray-500">
                <div>
                  <dt class="sr-only">Název společnosti</dt>
                  <dd>
                    <p>SmartBridge s.r.o.</p>
                  </dd>
                </div>
                <div>
                  <dt class="sr-only">Adresa</dt>
                  <dd>
                    <p>Na Bateriích 822/9</p>
                    <p>16200 Praha 6 - Střešovice</p>
                  </dd>
                </div>
                <div class="mt-6">
                  <dt class="sr-only">Kontaktní osoba</dt>
                  <dd class="flex">
                    <div class="flex-shrink-0 h-6 w-6 text-gray-400" aria-hidden="true">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="h-6 w-6"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        stroke-width="2"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
                        />
                      </svg>
                    </div>
                    <span class="ml-3"> Martin Bek </span>
                  </dd>
                </div>
                <!--                <div class="mt-3">-->
                <!--                  <dt class="sr-only">Telefon</dt>-->
                <!--                  <dd class="flex">-->
                <!--                    <div class="flex-shrink-0 h-6 w-6 text-gray-400" aria-hidden="true">-->
                <!--                      <svg-->
                <!--                        xmlns="http://www.w3.org/2000/svg"-->
                <!--                        class="h-6 w-6"-->
                <!--                        fill="none"-->
                <!--                        viewBox="0 0 24 24"-->
                <!--                        stroke="currentColor"-->
                <!--                        stroke-width="2"-->
                <!--                      >-->
                <!--                        <path-->
                <!--                          stroke-linecap="round"-->
                <!--                          stroke-linejoin="round"-->
                <!--                          d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"-->
                <!--                        />-->
                <!--                      </svg>-->
                <!--                    </div>-->
                <!--                    <span class="ml-3"> +420 000 000 000 </span>-->
                <!--                  </dd>-->
                <!--                </div>-->
                <div class="mt-3">
                  <dt class="sr-only">E-mail</dt>
                  <dd class="flex">
                    <div class="flex-shrink-0 h-6 w-6 text-gray-400" aria-hidden="true">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="h-6 w-6"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        stroke-width="2"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                        />
                      </svg>
                    </div>
                    <span class="ml-3"> <a href="mailto:bek@smartbridge.cz">bek@smartbridge.cz</a> </span>
                  </dd>
                </div>
                <div class="mt-8">
                  <dt class="sr-only">Identifikační číslo organizace</dt>
                  <dd class="flex">
                    <div class="flex-shrink-0 h-6 w-6 text-gray-400" aria-hidden="true">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="h-6 w-6"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        stroke-width="2"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          d="M8 14v3m4-3v3m4-3v3M3 21h18M3 10h18M3 7l9-4 9 4M4 10h16v11H4V10z"
                        />
                      </svg>
                    </div>
                    <span class="ml-3"> IČO: 02366762 </span>
                  </dd>
                </div>
              </dl>
            </div>
          </div>
          <div class="bg-white py-16 px-4 sm:px-6 lg:col-span-3 lg:py-24 lg:px-8 xl:pl-12">
            <div class="max-w-lg mx-auto lg:max-w-none">
              <form name="contact" method="POST" data-netlify="true" class="grid grid-cols-1 gap-y-6">
                <input type="hidden" name="subject" value="Zpráva odeslaná přes formulář na SmartBridge.cz" />
                <div>
                  <!-- eslint-disable-next-line -->
                  <label for="full-name" class="sr-only">Full name</label>
                  <input
                    id="full-name"
                    type="text"
                    name="full-name"
                    autocomplete="name"
                    class="block w-full shadow-sm py-3 px-4 placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md"
                    placeholder="Jméno"
                  />
                </div>
                <div>
                  <!-- eslint-disable-next-line -->
                  <label for="email" class="sr-only">Email</label>
                  <input
                    id="email"
                    name="email"
                    type="email"
                    autocomplete="email"
                    class="block w-full shadow-sm py-3 px-4 placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md"
                    placeholder="E-mail"
                  />
                </div>
                <div>
                  <!-- eslint-disable-next-line -->
                  <label for="phone" class="sr-only">Phone</label>
                  <input
                    type="text"
                    name="phone"
                    id="phone"
                    autocomplete="tel"
                    class="block w-full shadow-sm py-3 px-4 placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md"
                    placeholder="Telefonní číslo"
                  />
                </div>
                <div>
                  <!-- eslint-disable-next-line -->
                  <label for="message" class="sr-only">Zpráva</label>
                  <textarea
                    id="message"
                    name="message"
                    rows="4"
                    class="block w-full shadow-sm py-3 px-4 placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500 border border-gray-300 rounded-md"
                    placeholder="Vaše zpráva"
                  />
                </div>
                <div>
                  <button
                    type="submit"
                    class="inline-flex justify-center py-3 px-6 border border-transparent shadow-sm text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
                  >
                    Odeslat
                  </button>
                </div>
              </form>
            </div>
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
        { hid: 'description', name: 'description', content: 'Kontakt na SmartBridge s.r.o. - bek@smartbridge.cz' },
        { hid: 'og:image', name: 'og:image', content: '/empty.png' },
      ],
    };
  },
})
export default class Kontakt extends Vue {}
</script>
