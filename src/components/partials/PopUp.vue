<script>
export default {
    name: 'Pop-up',
    props: {
        popUp: Object,
        clicked: String
    }
}
</script>

<template>
  <div class="pop-up" :class="{'none' : clicked=false}">
     <span>&cross;</span>
       <h1>{{ popUp.brand }}</h1>  
       <p>{{ popUp.story }}</p> 
  </div>
</template>

<style lang="scss">
@use '../../scss/partials/variabiles' as *;

.pop-up{
    position: absolute;
    top:200px;
    left: 50%;
    transform: translate(-50%);
    z-index: 800;
    background-color: $white;
    border:1px solid $grey;
    padding: 40px;
    border-radius: 30px;
    span{
        float: right;
    }
}

</style>