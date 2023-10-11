<script>
import Menu from './partials/Menu.vue';
import productsMenu from '../data/menuProducts';

export default {
  name: 'Header',
  data() {
    return {
      productsMenu,

    }

  },
  components: {
        Menu,
    }  

}
</script>

<template>
      <header>
    <div class="topbar">
      <div class="container flex">
        <nav>
          <ul class="flex">
            <Menu 
            v-for="(section, index) in productsMenu" 
            :key="index" 
            :type="section.type"
            :link="section.link"
            />
          </ul>
        </nav>

        <div class="logo">        
          <img src="../../public/boolean-logo.png" alt="logo">
        </div>

        <nav class="flex">
          <a href="#"><i class="fa-regular fa-user"></i></a>
          <a href="#"><i class="fa-regular fa-heart"></i></a>
          <a href="#"><i class="fa-solid fa-bag-shopping"></i></a>
        </nav>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
@use '../scss/partials/variabiles' as *;

.topbar{
    background-color: $orange;
    width: 100%;
    height: 80px;
    position: fixed;
    top: 0;
    z-index: 999;
    box-shadow: 0 0 10px $grey;
    .container{
      justify-content: space-between;
      img{
        width: 100px;
        height: 25px;
      }
    }
  }
</style>