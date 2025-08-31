<template>
  <TheNavbar />
  <TheHome /> 
  <TheService /> 
  <TheAbout />
  <ThePopular />
  <TheReview />
</template>

<script>
import TheNavbar from './components/TheNavbar.vue';
import TheHome from './components/TheHome.vue';
import TheService from './components/TheService.vue';
import TheAbout from './components/TheAbout.vue';
import ThePopular from './components/ThePopular.vue';
import TheReview from './components/TheReview.vue';

export default {
  components: {
    TheNavbar,
    TheHome,
    TheService,
    TheAbout,
    ThePopular,
    TheReview,
  }
}
</script>

<style>
</style>
