<script>
import {store} from "../store.js";

export default {
  name: "AppTestimonialsBot",
    data() {
        return {
            store,
          };
        }, 


    components: {  },

    methods: {

    },
}

</script>

<template>
  <div class="main-container">
    <div class="left-section">
      <img src="/img/home-3-team-image.png" alt="">
      <img class="dot-round" src="/img/maxcoach-shape-05.png" alt="">
      <img class="dot-square" src="/img/maxcoach-shape-07.png" alt="">
      <img class="line" src="/img/maxcoach-shape-01.png" alt="">
      <img class="splash" src="/assets/svg-0.svg" alt="">
    </div>
    <div class="right-section">
      <span class="subtitle">EVERYTHING IN <strong>MAXCOACH</strong></span>
        <h2>We're Here To <span class="titleColored">Transform</span> You!</h2>
        <p>As learners, people can enjoy great companionship from MaxCoach mentors and educators. We can help you develop and grow at your best.</p>
        <button>Get Free Guide</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.main-container{
  max-width: 1200px;
  margin: auto;
  padding-top: 300px;
  display: flex;
  .left-section{
    position: relative;
    .dot-round{
      position: absolute;
      left: -150px;
      bottom: 150px;
    }
    .dot-square{
      position: absolute;
      bottom: -90px;
      left: 230px;
      z-index: -1;
    }
    .line{
      position: absolute;
      left: -250px;
      bottom: 0;
    }
    .splash{
      position: absolute;
      left: -50px;
      z-index: -1;
      filter: invert(85%) sepia(27%) saturate(396%) hue-rotate(117deg) brightness(91%) contrast(88%);
    }
  }
  .left-section::after{
          content: '';
          width: 60px;
          height: 60px;
          position: absolute;
          border: 10px solid #ecc5ab;
          border-radius: 50%;
        }
  .right-section{
    padding-top: 100px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
    .subtitle{
      color: gray;
    }
    h2{
      font-size: 3.5em;
      .titleColored{
        color: #20ad96;
        font-weight: 300;
      }
    }
    button{
      padding: 15px 40px;
      border-radius: 5px;
      color: white;
      font-weight: bold;
      background-color: #20ad96;
      border: 0;
    }
  }
}
</style>