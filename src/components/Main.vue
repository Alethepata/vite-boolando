<script>
import ProductCard from './partials/ProductCard.vue';
import cards from '../data/products';

export default {
  components: { ProductCard },
  name: 'Main',
  data() {
    return {
      cards,
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

        <ProductCard 
        v-for="(card,index) in cards" 
        :key="index" 
        :cardObj="card"
        />

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

