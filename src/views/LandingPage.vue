<template>
  <div class="landing">
    <figure class="landing__logo">
      <img src="../assets/images/Logo.svg" alt="">
    </figure>
    <search-form />
    <carousel /> 
  </div>
</template>
<script>
import SearchForm from '../components/SearchForm.vue'
import Carousel from '../components/Carousel.vue'

export default {
  name: 'LandingPage',
  components: {
    SearchForm,
    Carousel
  },
  data() {
    return {
      isModalVisible: false
    }
  },
  methods: {
    
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