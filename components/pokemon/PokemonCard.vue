<template>
  <div class="py-8">
    <div
      class="mx-auto p-2 lg:w-1/3 md:w-1/2 w-full cursor-pointer"
      @click.prevent="goToDetailPage(pokemonData.id)"
    >
      <div
        class="h-full flex items-center border-gray-200 border p-4 rounded-lg"
      >
        <img
          alt="team"
          class="w-16 h-16 bg-gray-100 object-cover object-center flex-shrink-0 rounded-full mr-4"
          :src="pokemonData.sprites.front_default"
        />
        <div class="flex-grow">
          <h2 class="text-gray-900 title-font font-medium capitalize">
            {{ pokemonData.name }}
          </h2>
          <p class="text-gray-500">
            Types:
            <span> {{ getTypes(pokemonData.types) }} </span>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'PokemonCard',
  props: {
    pokemonInfo: { type: Object, default: null },
  },
  computed: {
    pokemonData() {
      return this.pokemonInfo
    },
  },
  methods: {
    getTypes(types) {
      return types.map((type) => type.type.name).join(', ')
    },
    goToDetailPage(pokemonId) {
      this.$router.push({ path: `/pokemon/details/${pokemonId}` })
    },
  },
}
</script>
