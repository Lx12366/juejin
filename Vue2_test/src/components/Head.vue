<template>
  <div id="header">
    <div class="container">
      <a href="/" class="logo">
        <img src="../assets/img/002.png" alt="稀土掘金">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name:'Head'
} 
</script>

<style>
  #header{
    color: #909090;
    border-bottom: 1px solid #f1f1f1;
    height: 5rem;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    transition: all .2s;
    transform: translateZ(0);
  }

  .logo{
    margin-right: 1rem;
    margin-left: 24px;
    display: inline-block;
    height: 22px;
    width: auto;
  }
</style>