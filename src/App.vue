/* eslint-disable no-undef */
/* eslint-disable eol-last */
<template>
  <div id="app">
    <aside-menu></aside-menu>
    <div class="mask-map" id="mask-map"></div>
    <lightbox></lightbox>
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import asideMenu from './components/asideMenu.vue';
import lightbox from './components/lightbox.vue';

export default {
  name: 'App',
  components: {
    asideMenu,
    lightbox,
  },
  mounted() {
    this.$store.dispatch('fetchLocations');
    this.$store.dispatch('fetchPharmacies');
  },
};
</script>


<style lang="scss" src="./scss/all.scss"></style>
