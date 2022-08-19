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
    list-style: none;

  }
  html,body{
    width: 100%;
    height: 100%;
      font-size: 12px;
  }
 
</style>
