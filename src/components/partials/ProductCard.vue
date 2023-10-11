<script>
import PopUp from './PopUp.vue'
export default {
  name: 'ProductCard',
  data() {
    return {
      like: false,
      clicked: false
    }
    
  },
  components: {
    PopUp
  },
  props: {
    cardObj:Object

  },
  methods: {
    getImg(img) {
      return new URL (`../../assets/img/${img}`, import.meta.url).href
      
    },
    likeHeart() {
      this.like = !this.like
    },
    getClick() {
      this.clicked = !this.clicked
    }
  
}

}
</script>

<template>
  
  <div class="card" @click="getClick()">
    <PopUp :class="{'none' : !clicked}" :popUp="cardObj" :clicked="clicked"/>

<div class="contenuto-card">
  <div class="image-card">

    <img class="first-img"  :src="getImg(cardObj.imageFirst)" alt="item">
     <img class="second-img" :src="getImg(cardObj.imageSecond)" alt="item">

  </div>

  <div class="discount">
    <span class="discount-red" v-if="cardObj.discount">{{ cardObj.discount}}</span>
    <span class=" discount-green" v-if="cardObj.sustainability">Sostenibilità</span>
  </div>

  <div class="heart" @click="likeHeart()">
    <span :class="{'like-color' : like}">&hearts;</span>
  </div>
</div>

<div class="text">
  <span>{{ cardObj.brand}}</span>
  <span>{{ cardObj.description}}</span>
</div>

<div class="prezzo">
  <span>{{ cardObj.discountedPrice}}</span>
  <span :class="{'line-through' : cardObj.discountedPrice}">{{cardObj.price}}</span>
</div>

</div>

</template>

<style lang="scss">
@use '../../scss/partials/variabiles' as *;

.like-color{
  color: $red;
}
.none{
  display: none;
}

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
  .second-img{
    position: absolute;
    top: 0;
    left: 0;
    display: none;
  }
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
  .text{
     span{
      display: block;
      &:first-child{
        font-size: 12px;
      }
      &:last-child{
        font-weight: 600;
      }
  }
  }      

  }  
  .prezzo{
     span{
      margin-right: 10px;
    &:first-child{
      color: $red;
    }
    &:first-child{
    font-weight: 600;

  }
  }
  }


</style>
