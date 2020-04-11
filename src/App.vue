/* eslint-disable eol-last */
<template>
  <div id="app">
    <!-- aside-menu 左側欄 -->
    <asideMenu></asideMenu>
    <!-- 地圖區塊 -->
    <div class="mask-map" id="mask-map"></div>
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import asideMenu from './components/asideMenu.vue';

export default {
  name: 'App',
  components: {
    asideMenu,
  },
  mounted() {
    this.$store.dispatch('fetchLocations');
    this.$store.dispatch('fetchPharmacies');
  },
};
</script>


<style lang="scss" src="./scss/all.scss"></style>
