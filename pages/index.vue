
<template>
  <div>
    <barSearch />
    <databar />
    <weatherData />
  </div>
</template>
<script>
  import barSearch from '@/components/barSearch';
  import databar from '@/components/databar';
  import weatherData from '@/components/weatherData';

  export default {
    components: {
      barSearch,
      databar,
      weatherData
    }
  }
</script>

<style>

</style>