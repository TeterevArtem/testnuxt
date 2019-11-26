<template>
  <div>
    <header class="header">
      <Header/>
    </header>
    <main class="main container">
      <nuxt/>
    </main>
    
  </div>
</template>

<script>

import Header from '~/components/Header'

export default {
  components: {
    Header
  }
}
</script>

<style lang="scss">
  .header{
    box-shadow: 0 2px 3px rgba(0,0,0,.3);
    margin-bottom: 40px;
  }
  html, body{
    width: 100%;
    height: 100%;
    background: radial-gradient(circle at center, #f9f9f9, #ddd) center center
  }
</style>

