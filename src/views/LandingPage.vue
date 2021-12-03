<template>
  <div class="landing">
    <figure class="landing__logo">
      <img src="../assets/images/Logo.svg" alt="">
    </figure>
    <search-bar />
    <search-button @click="showModal"/>
    <carousel /> 
    <results-modal v-show="isModalVisible" />
  </div>
</template>
<script>
import SearchBar from '../components/SearchBar.vue'
import Carousel from '../components/Carousel.vue'
import ResultsModal from '../components/ResultsModal.vue'
import SearchButton from '../components/Button.vue'

export default {
  name: 'LandingPage',
  components: {
    SearchBar,
    Carousel,
    ResultsModal,
    SearchButton
  },
  data() {
    return {
      isModalVisible: false
    }
  },
  methods: {
    showModal() {
      console.log('clicked')
      this.isModalVisible = true
    },
    closeModal() {
      this.isModalVisible = false
    }
  }
}
</script>
<style lang="scss" scoped>
@import '../assets/css/global-styles'; 

.landing {
 display: flex;
 flex-direction: column;

 &__logo {
   margin: 30px auto;
 }
}
</style>