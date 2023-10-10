<script>
export default {
    name:'Main'
}
</script>

<template>
      <main>
    <div class="card-container container flex">
      <div class="card">
        <div class="contenuto-card">
          <div class="image-card">
            <img class="first-img"  src="../assets/img/1.webp" alt="item">
            <img class="second-img" src="../assets/img/1b.webp" alt="item">
          </div>
          <div class="discount">
            <span class="discount-red">-50%</span>
            <span class=" discount-green">Sostenibilità</span>
          </div>
          <div class="heart">
            <span>&hearts;</span>
          </div>
        </div>
        <div class="text">
          <span>Levi's</span>
          <span>RELAXED FIT TEE UNISEX</span>
        </div>
        <div class="prezzo">
          <span>14,99 &euro;</span>
          <span class="line-through">29,99 &euro;</span>
        </div>
      </div>
      <div class="card">
        <div class="contenuto-card">
          <div class="image-card">
            <img class="first-img"  src="../assets/img/2.webp" alt="item">
            <img class="second-img" src="../assets/img/2b.webp" alt="item">
          </div>
          <div class="discount">
            <span class="discount-red">-50%</span>
          </div>
          <div class="heart">
            <span>&hearts;</span>
          </div>
        </div>
        <div class="text">
          <span>Guess</span>
          <span>ROSES TEE</span>
        </div>
        <div class="prezzo">
          <span>20,99 &euro;</span>
          <span class="line-through">29,99 &euro;</span>
        </div>
      </div>
      <div class="card">
        <div class="contenuto-card">
          <div class="image-card">
            <img class="first-img"  src="../assets/img/3.webp" alt="item">
            <img class="second-img" src="../assets/img/3b.webp" alt="item">
          </div>
          <div class="discount">
            <span class="discount-red">-50%</span>
          </div>
          <div class="heart">
            <span>&hearts;</span>
          </div>
        </div>
        <div class="text">
          <span>Come zucchero filato</span>
          <span>VOGLIA DI COLORI PASTELLO</span>
        </div>
        <div class="prezzo">
          <span>129,99 &euro;</span>
          <span class="line-through">184,99 &euro;</span>
        </div>
      </div>
      <div class="card">
        <div class="contenuto-card">
          <div class="image-card">
            <img class="first-img"  src="../assets/img/4.webp" alt="item">
            <img class="second-img" src="../assets/img/4b.webp" alt="item">
          </div>
        <div class="discount">
          <span class="discount-red">-50%</span>
          <span class=" discount-green">Sostenibilità</span>
        </div>
        <div class="heart">
          <span>&hearts;</span>
        </div>
        </div>
        <div class="text">
          <span>Levi's</span>
          <span>TEE UNISEX</span>
        </div>
        <div class="prezzo">
          <span>14,99 &euro;</span>
          <span class="line-through">29,99 &euro;</span>
        </div>
      </div>
      <div class="card">
        <div class="contenuto-card">
          <div class="image-card">
            <img class="first-img"  src="../assets/img/5.webp" alt="item">
            <img class="second-img" src="../assets/img/5b.webp" alt="item">
          </div>
          <div class="heart">
            <span>&hearts;</span>
          </div>
        </div>
        <div class="text">
          <span>Maya Deluxe</span>
          <span>STRIPE BODICE</span>
        </div>
        <div class="prezzo">
          <span>99,99 &euro;</span>
        </div>
      </div>
      <div class="card">
        <div class="contenuto-card">
          <div class="image-card">
            <img class="first-img"  src="../assets/img/6.webp" alt="item">
            <img class="second-img" src="../assets/img/6b.webp" alt="item">
          </div>
          <div class="discount">
            <span class=" discount-green">Sostenibilità</span>
          </div>
          <div class="heart">
            <span>&hearts;</span>
          </div>
        </div>
        <div class="text">
          <span>Espirit</span>
          <span>MAGLIONE-BLACK</span>
        </div>
        <div class="prezzo">
          <span>29,99 &euro;</span>
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

