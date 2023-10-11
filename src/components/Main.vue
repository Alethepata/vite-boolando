<script>
import ProductCard from './partials/ProductCard.vue';

export default {
  components: { ProductCard },
  name: 'Main',
  data() {
    return {
      components: {
        ProductCard
      }
    }

  }
}

</script>

<template>
<main>
      <div class="card-container container flex">

        <ProductCard/>

    </div>
</main>
</template>

<style lang="scss">

main{
    margin-top: 80px ;

    .card-container{
    flex-wrap: wrap;
    justify-content: space-between;
    }
  }

</style>

