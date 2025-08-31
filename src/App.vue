<template>
  <TheNavbar />
  <TheHome /> 
  <TheService /> 
  <TheAbout />
  <ThePopular />
</template>

<script>
import TheNavbar from './components/TheNavbar.vue';
import TheHome from './components/TheHome.vue';
import TheService from './components/TheService.vue';
import TheAbout from './components/TheAbout.vue';
import ThePopular from './components/ThePopular.vue';

export default {
  components: {
    TheNavbar,
    TheHome,
    TheService,
    TheAbout,
    ThePopular,
  }
}
</script>

<style>
</style>
