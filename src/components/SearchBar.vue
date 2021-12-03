<template>
  <div class="search-bar">
    <label for="search">Find a Pokemon</label>
    <input type="search" name="filterList" id="" class="search-bar__input" required>
  </div>
</template>
<script>
export default {
  name: 'SearchBar',
}
</script>
<style lang="scss" scoped>
@import '../assets/css/global-styles';

.search-bar {
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
</style>