<script>
export default {
  name: 'Header'
}
</script>


<template>
  <header>
    
    <img src="/logo_yu-gi-oh.webp" alt="">
    <h1>Yu-Gi-Oh API</h1>

  </header>
</template>


<style lang="scss" scoped>

@use '../scss/main.scss' as *;

header {
  display: flex;
  align-items: center;
  width: 100%;
  height: 40px;

  img {
    width: 50px;
  }
}


</style>