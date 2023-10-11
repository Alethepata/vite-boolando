<script>
export default {
    name:'Footer'
}
</script>

<template>
    <footer>
       <div class="container">
         <div class="second-text float">
           <h4>Boolando s.r.l</h4>
           <nav>
             <ul class="flex">
               <li><a href="#">Informazioni legali</a></li>
               <li><a href="#">Informativa sulla privacy</a></li>
               <li><a href="#">Diritto di recesso</a></li>
             </ul>
           </nav>
         </div>
         <div class="social">
           <h4>Trovaci anche su</h4>
           <nav>
             <a href="#"><i class="fa-brands fa-square-twitter"></i></a>
             <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
             <a href="#"><i class="fa-brands fa-square-instagram"></i></a>
             <a href="#"><i class="fa-brands fa-square-pinterest"></i></a>
             <a href="#"><i class="fa-brands fa-square-youtube"></i></a>
           </nav>
         </div>
       </div>
    </footer>
</template>

<style lang="scss">
@use '../scss/partials/variabiles' as *;

footer{
    background-color: $footer;
    height: 100px;
    color: $white;
    padding-top: 20px;

    .second-text{
    float: left;
  }    
  .social{
    float: right;
  }

  }

</style>