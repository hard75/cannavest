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
  * {
    color: #0B3842;
  }

  html {
    font-family: "adobe-clean", sans-serif;
  }

  .general-margin {
    width: 1711px;
    margin-right: auto;
    margin-left: auto;
  }
</style>
