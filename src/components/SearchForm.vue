<template>
  <div class="search-form">
    <div class="search-form__search-bar">
      <label for="search">Find a Pokemon</label>
      <input type="search" name="filterList" id="" class="search-form__search-bar__input" v-model="userQuery" required>
    </div>
    <search-button @open="displayModal"/>
    <results-modal v-show="showModal" :queryFilter="this.userQuery" :results="this.pokemonList"/>
  </div>
</template>
<script>
import SearchButton from '../components/Button.vue'
import ResultsModal from '../components/ResultsModal.vue'

export default {
  name: 'SearchForm',
  components: {
    SearchButton,
    ResultsModal
  },
  data() {
    return {
      pokemonList: {},
      showModal: false,
      userQuery: '',
      filteredResults: []
    }
  },
  methods: {
    getDataFromApi() {
      fetch(`https://pokeapi.co/api/v2/pokemon/${this.userQuery}`)
      .then(response => response.json())
      .then(data => this.pokemonList = data.results)
    },
    displayModal() {
      this.getDataFromApi()
      this.showModal = true
    },
    closeModal() {
      this.showModal = false
    },
    filterList() {

    }
  },
}
</script>
<style lang="scss" scoped>
@import '../assets/css/global-styles';

.search-form {
  &__search-bar {
  display: flex;
  flex-direction: column;
  margin: 20px auto;
  width: 90%;
  text-align: center;
  color: $white;
  

  &__input {
    height: 50px;
    border-radius: 10px;
    border: none;
    box-shadow: $global-box-shadow;
    padding: 20px;
    margin: 10px 0;
  }
}
}
</style>