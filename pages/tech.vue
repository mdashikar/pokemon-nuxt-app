<template>
  <div>
    <section class="text-gray-600 body-font">
      <div class="container px-5 py-24 mx-auto">
        <div class="text-center mb-8">
          <h1
            class="sm:text-3xl text-2xl font-medium text-center title-font text-gray-900 mb-4"
          >
            A Pokémon Application with Nuxt
          </h1>
          <p class="text-base leading-relaxed xl:w-2/4 lg:w-3/4 mx-auto">
            This app will let you search pokemon through pokeapi and see info of
            that pokemon.
          </p>
        </div>
        <div class="flex flex-wrap lg:w-4/5 sm:mx-auto sm:mb-2 -mx-2">
          <div
            v-for="(tech, index) in technologies"
            :key="index"
            class="p-2 sm:w-1/2 w-full"
          >
            <div class="bg-gray-100 rounded flex p-4 h-full items-center">
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="3"
                class="text-indigo-500 w-6 h-6 flex-shrink-0 mr-4"
                viewBox="0 0 24 24"
              >
                <path d="M22 11.08V12a10 10 0 11-5.93-9.14"></path>
                <path d="M22 4L12 14.01l-3-3"></path>
              </svg>
              <span class="title-font font-medium">{{ tech }}</span>
            </div>
          </div>
        </div>
        <a
          class="flex w-2/12 mx-auto mt-16 text-white bg-gray-900 hover:bg-gray-800 border-0 py-2 px-8 focus:outline-none rounded text-lg"
          target="_blank"
          href="https://github.com/mdashikar/pokemon-app-nuxt"
        >
          Source Code
        </a>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  name: 'Tech',
  data() {
    return {
      technologies: [
        'HTML',
        'CSS',
        'Tailwind',
        'JavaScript',
        'VueJs',
        'NuxtJs',
        'Poke restAPi',
      ],
    }
  },
}
</script>
