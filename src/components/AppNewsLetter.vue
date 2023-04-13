<script>
import {store} from "../store.js";

export default {
  name: "AppNewsLetter",
    data() {
        return {
            store,
        };
    }, 

    components: {  },
}

</script>

<template>
  <div class="background">
   <div class="main-container">
    <h2 class="title">Subscribe <span class="titleColored">Newsletters</span></h2>
    <span class="description">Enter your email address to register to our newsletter subscription delivered on a regular basis!</span>
    <div class="form-email">
      <input type="email" placeholder="Enter your email">
      <button>Subscribe</button>
    </div>
    <img class="square" src="/img/maxcoach-shape-09.png" alt="">
    <img class="circle" src="/img/maxcoach-shape-02.png" alt="">
   </div>
  </div>
</template>

<style scoped lang="scss">
.background{
  position: relative;
  .main-container::before{
    content: '';
          width: 60px;
          height: 60px;
          position: absolute;
          border: 10px solid #20ad956e;
          border-radius: 50%;
          left: 0px;
          top: 200px;
  }
  .main-container{
    max-width: 1200px;
    margin: auto;
    padding-top: 100px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 40px;
    padding-bottom: 100px;
    position: relative;
    .title{
      font-size: 3.5em;
      font-weight: 700;
      .titleColored{
        color: #20AD96;
        font-weight: 500;
      }
    }
    .description{
      font-size: 1.2em;
      max-width: 60%;
      text-align: center;
      color: rgb(82, 82, 82);
      font-weight: 500;
    }
    .form-email{
      input{
        background-color: #f5f5f5;
        padding: 20px 15px 20px 15px;
        border: 0;
        border-radius: 10px 0px 0px 10px;
        width: 500px;
      }
      button{
        padding: 20px 15px 20px 15px;
        border: 0;
        border-radius: 0px 10px 10px 0px;
        background-color: #20AD96;
        color: white;
        font-size: 1em;
      }
    }
    .square{
      position: absolute;
      right: 0;
      top: 60px;
    }
    .circle{
      position: absolute;
      top: 165px;
      right: 0;
    }
  }
}

</style>