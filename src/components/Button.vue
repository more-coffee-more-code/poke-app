<template>
  <button type="submit" class="button" @click="getDataFromApi">Go</button>
</template>
<script>
export default {
  name: 'Button',
  methods: {
    triggerModal() {
      this.$emit('open')
    },
    getDataFromApi() {
      fetch("https://pokeapi.co/api/v2/pokemon?limit=50")
      .then(response => response.json())
      .then(data => data)
    },
  }
}
</script>
<style lang="scss" scoped>
@import '../assets/css/global-styles';

.button {
  background-color: $poke-yellow;
  padding: 20px;
  width: 100px;
  color: $poke-red;
  border-radius: 20px;
  border: none;
  margin: 20px auto;
  box-shadow: $global-box-shadow;
  font-weight: bold;
  font-size: 30px;
  cursor: pointer;
}
</style>