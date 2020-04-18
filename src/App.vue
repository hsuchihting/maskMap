/* eslint-disable no-undef */
/* eslint-disable no-undef */
/* eslint-disable eol-last */
<template>
  <div id="app">
    <aside-menu></aside-menu>
    <maskmap></maskmap>
    <lightBox></lightBox>
  </div>
</template>

<script>

import asideMenu from './components/asideMenu.vue';

import lightBox from './components/lightbox.vue';

import maskMap from './components/maskMap.vue';

export default {
  name: 'App',
  components: {
    asideMenu,
    lightBox,
    maskMap,
  },
  mounted() {
    this.$store.dispatch('fetchLocations');
    this.$store.dispatch('fetchPharmacies');
  },
};
</script>


<style lang="scss" src="./scss/all.scss"></style>
