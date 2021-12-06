<template>
  <div class="results-modal">
    <ul>
      <li v-for="result in results" :key="result">{{result.name}}</li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'ResultsModal',
  props: {
    results: Object,
    queryFilter: String
  }
}
</script>
<style lang="scss" scoped>
@import '../assets/css/global-styles';

.results-modal {
  background-color: $poke-yellow;
  color: $poke-red;
  position: absolute;
  top: 0;
  z-index: 9999;
  width: 100%;
  height: 100%;
  overflow: scroll;
}
</style>