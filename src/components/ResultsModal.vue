<template>
  <div class="results-modal">
    {{pokemonList}}
  </div>
</template>
<script>
export default {
  name: 'ResultsModal',
  data() {
    return {
      showModal: true,
      pokemonList: []
    }
  },
  created() {
    this.getDataFromApi()
  },
  methods: {
    getDataFromApi() {
      fetch("https://pokeapi.co/api/v2/pokemon?limit=50")
      .then(response => response.json())
      .then(data =>  this.pokemonList = data)
    },
  }
}
</script>
<style lang="scss" scoped>
@import '../assets/css/global-styles';

.results-modal {
  background-color: $poke-yellow;
  color: $poke-red;
}
</style>