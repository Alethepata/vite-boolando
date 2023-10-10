<script>
export default {
  name: 'Main',
  data() {
    return {
      cards: [
        {
          brand: 'Levi\'s',
          description: 'RELAXED FIT TEE UNISEX',
          discount: '-50%', 
          sustainability: true,
          price: '€ 29,99',
          discountedPrice: '€ 14,99',
          image: '1.webp',

        },
        {
          brand: 'Guess',
          description: 'ROSES TEE',
          discount: '-50%', 
          sustainability: false,
          price: '€ 29,99',
          discountedPrice: '€ 20,99',
          image: '2.webp',

        },
        {
          brand: 'Come zucchero filato',
          description: 'VOGLIA DI COLORI PASTELLO',
          discount: '-50%', 
          sustainability: false,
          price: '€ 184,99',
          discountedPrice: '€ 129,99',
          image: '3.webp',

        },
        {
          brand: 'Levi\'s',
          description: 'TEE UNISEX',
          discount: '-50%', 
          sustainability: true,
          price: '€ 29,99',
          discountedPrice: '€ 14,99',
          image: '4.webp',

        },
        {
          brand: 'Maya Deluxe',
          description: 'STRIPE BODICE',
          discount: null, 
          sustainability: false,
          price: '€ 99,99',
          discountedPrice: null,
          image: '5.webp',

        },
        {
          brand: 'Espirit',
          description: 'MAGLIONE-BLACK',
          discount: null, 
          sustainability: true,
          price: '€29,99',
          discountedPrice: null,
          image: '6.webp',

        }
        ]
      }
  },
//   methods: {
//     getImg(img) {
//       return new URL (`../assets/img/${img}`, import.meta.url).href
      
//     }
  
// }
}

</script>

<template>
      <main>
    <div class="card-container container flex">
      <div class="card"   v-for="(card,index) in cards" :key="index">
        <div class="contenuto-card">
          <div class="image-card">
            <img class="first-img"  src="../assets/img/1.webp" alt="item">
            <img class="second-img" src="../assets/img/1b.webp" alt="item">
            <!-- <img class="first-img"  :src="getImg()" alt="item">
            <img class="second-img" :src="getImg()" alt="item"> -->
          </div>
          <div class="discount">
            <span class="discount-red" v-if="card.discount">{{ card.discount}}</span>
            <span class=" discount-green" v-if="card.sustainability">Sostenibilità</span>
          </div>
          <div class="heart">
            <span>&hearts;</span>
          </div>
        </div>
        <div class="text">
          <span>{{ card.brand}}</span>
          <span>{{ card.description}}</span>
        </div>
        <div class="prezzo">
          <span>{{ card.discountedPrice}}</span>
          <span :class="{'line-through' : card.discountedPrice}">{{card.price}}</span>
        </div>
      </div>

    </div>
  </main>
</template>

<style lang="scss">
@use '../scss/partials/variabiles' as *;

main{
    margin-top: 80px ;

    .card-container{
    flex-wrap: wrap;
    justify-content: space-between;

    .card{
    padding: 40px 15px 0 0;
    cursor: pointer;

    .contenuto-card{
    position: relative;

    .image-card{

      &:hover .second-img {
      display: block;
  }

    display: block;
    
    img{
    width: 300px;

  }

  
  
  }
  .second-img{
    position: absolute;
    top: 0;
    left: 0;
    display: none;
  }
  .discount{
  position: absolute;
  bottom: 30px;
  .discount-red,.discount-green{
    padding: 5px; 
    font-size: 14px;
  }
  .discount-red{
    background-color: $red;
    color: $white;
  }
  .discount-green{
    background-color: $green;
    color: $white;
   }
   }
  .heart{
    position: absolute;
    top: 0;
    right: 0;
    background-color: $white;
    padding: 5px 10px;
    font-size: 20px;
  } 
  }
  .text span{
    display: block;
  }      
  .text span:first-child{
    font-size: 12px;
  }
  .text span:last-child,.prezzo span:first-child{
    font-weight: 600;
  }  
  .prezzo span:first-child{
    color: $red;
  }

  }

  }

  }

</style>

