<script >
  
  import AppHeader from './components/AppHeader.vue'
  import AppNav from './components/AppNav.vue'
  
  
  

  export default {
  components:{  AppHeader,  AppNav}
  }
</script>

<template>

  <div class="container">
    <div class="top">
      <AppHeader class="header"/>
    </div>
    <div class="bottom">
      <AppNav class="nav"/>
      <router-view class="page"></router-view>
    </div>
  </div>
 

  
</template>

<style lang="scss">
@use './assets/styles/general.scss' as *;

.container{
  width: 100vw;
  height: 100%;
  .top{
    height: 20vh;
    width: 100%;
  }
  .bottom{
    display: flex;
    height: 80vh;

    .nav{
      width: 20%;
      height: 80vh;
    }
    .page{
      width: 80%;
    }
  }
 
}

@media (max-width: 1600px) {
  .nav{
    display: none !important;
  }
  .page{
    width: 100%!important;
  }
  
}


</style>
