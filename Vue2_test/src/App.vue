<template>
  <div id="app" class="container">
    <Head></Head>
  </div>
</template>

<script>
import Head from './components/Head'

export default {
  name: 'App',
  components:{Head}
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;

  }
  html{
      font-size: 12px;
  }
  .container{
    position: relative;
    width:100%;
  }
</style>
