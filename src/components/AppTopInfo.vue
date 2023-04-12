<script>
import {store} from "../store.js";

export default {
  name: "AppTopInfo",
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
      <div class="top-section">
        <div class="left-section">
          <span class="subtitle">EVERYTHING IN <strong>MAXCOACH</strong></span>
          <h2>Learn about our <span class="thin-font">Work Culture</span> at MaxCoach</h2>
          <p>Spend some time to visit our website or head office and discover our current courses, enrollment procedure, and registration deadline. We're openening new classes every beginning of each month.</p>
          <span>Have questions? <a href="#">Get free guide <i class="fa-solid fa-arrow-right"></i></a></span>
        </div>
        <div class="right-section">
          <div class="img-container">
            <img class="small-img" src="/img/about-us-01-ohkia3qg98rq9vg3s0mn2hkflr1migdqdw370qnegc.jpg" alt="">
            <img class="main-img" src="/img/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg" alt="">
            <img class="round-img" src="/img/maxcoach-shape-02.png" alt="">
            <img class="back-img" src="/img/maxcoach-shape-07.png" alt="">
          </div>
        </div>
      </div>
      <div class="bot-section">
        <div>
          <h2>129+</h2>
          <span>ENROLLED LEARNERS</span>
        </div>
        <div>
          <h2>80</h2>
          <span>FINISHED SESSION</span>
        </div>
        <div>
          <h2>4%</h2>
          <span>SATISFACTION RATE</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.background{
  .main-container{
    padding-top: 100px;
    max-width: 1200px;
    margin: auto;
    .top-section{
      display: flex;
      .left-section{
        display: flex;
        flex-direction: column;
        padding-right: 40px;
        padding-top: 40px;
        gap: 10px;
        color: #696969;

        h2{
          color: black;
          font-size: 2.5em;
        }
        .thin-font{
          font-weight: 400;
          color: #20AD96;
        }
        span{
          a{
            color: #20AD96;
          }
        }
      
      }
      .right-section{
        .img-container{
          position: relative;
          .small-img{
            position: absolute;
            top: -40px;
            right: -60px;
            border-radius: 5px;
            z-index: 2;
          }
          .main-img{
            padding-left: 200px;
            padding-top: 50px;
          }
          .round-img{
            position: absolute;
            bottom: -100px;
            right: 50px;
          }
          .back-img{
            position: absolute;
            top: -30px;
            right: 10px;
            border-radius: 5px;
            z-index: -1;
          }

        }
        .img-container::before{
          content: '';
          width: 60px;
          height: 60px;
          position: absolute;
          border: 10px solid #ecc5ab;
          border-radius: 50%;
        }
      }

    }
    .bot-section{
      padding-top: 150px;
      display: flex;
      justify-content: center;
      gap: 40px;
      div{
        display: flex;
        flex-direction: column;
        align-items: center;
        h2{
          font-weight: bold;
          color: #20AD96;
          font-size: 2.8em;
        }
        span{
          font-weight: 600;
          color: #696969;
          font-size: 1.2em
        };
      }
    }
  }
}

@media screen and (max-width: 1200px) {
  .small-img{
    display: none;
  }
}


</style>