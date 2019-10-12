<template>
  <div>
    <img src="../../public/img/index.jpg" alt="" class="index mt-5">
    <br>
    
    <div class="center">
      <router-link :to="{path:'/login'}"><button class="btn button" > Enter Site </button> </router-link>
    </div>
    <br>
    <div class="center ">
      <img class="logo mr-3 ml-3" src="../../public/img/Gear.png" alt="">
      <img class="logo mr-3 ml-3" src="../../public/img/cpe.png" alt="">
    </div>
    <br>
    <p class="center index-text">
      - Department of Computer Engineering, Chiang Mai University -
    </p>
    
    
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
  .logo{
    max-width: 5%;
  }
  .index{
    position: relative;
    display: block;
    max-width: 80%;
    
    border-radius: 5px;
    box-shadow: 0px 2px 7px #505050;
    
    margin-left: auto;
    margin-right: auto;
    
  }
  .center{
    text-align :center;
  }
  .button{
    border-radius: 25px;
    background-color:rgb(27, 27, 27);
    color: white;
  }
  .index-text{
    color:rgb(51, 51, 51);
    font-size: 18px;
  }
</style>