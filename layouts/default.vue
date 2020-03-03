<template>
  <div class="general-margin">
    <mainMenu />
    <nuxt />
  </div>
</template>

<script>
import mainMenu from '@/components/mainMenu'
export default {
  components: {
    mainMenu
  }
}
</script>

<style>
  html {
    font-family: 'Open Sans', ;
  }

  .general-margin {
    width: 1711px;
    margin-right: auto;
    margin-left: auto;
  }
</style>
