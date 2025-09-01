<template>
  <TheNavbar />
  <TheHome /> 
  <TheService /> 
  <TheAbout />
  <ThePopular />
  <TheReview />
  <TheFooter />
</template>

<script>
import TheNavbar from './components/TheNavbar.vue';
import TheHome from './components/TheHome.vue';
import TheService from './components/TheService.vue';
import TheAbout from './components/TheAbout.vue';
import ThePopular from './components/ThePopular.vue';
import TheReview from './components/TheReview.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  components: {
    TheNavbar,
    TheHome,
    TheService,
    TheAbout,
    ThePopular,
    TheReview,
    TheFooter,
  }
}
</script>

<style>
</style>
