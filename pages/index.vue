
<template>
  <div>
    <menubar @closeMenu="closeMainMenu" :visibleMenu="isVisibleMenu" />
    <barSearch />
    <databar />
    <weatherData />
    <tableGraph />
    <mainFooter />
  </div>
</template>
<script>
  import barSearch from '@/components/barSearch';
  import databar from '@/components/databar';
  import weatherData from '@/components/weatherData';
  import tableGraph from '@/components/tableGraph';
  import mainFooter from '@/components/mainFooter';
  import menubar from '@/components/menubar';

  export default {
    data () {
      return {
        isVisibleMenu: false
      }
    },
    components: {
      barSearch,
      databar,
      weatherData,
      tableGraph,
      mainFooter,
      menubar
    },
    methods: {
      closeMainMenu () {

      }
    }
  }
</script>

<style>

</style>