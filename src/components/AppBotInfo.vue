<script>
import {store} from "../store.js";

export default {
  name: "AppBotInfo",
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
      <div class="left-section">
        <div class="img-container">
          <img src="/img/stock-full-hd-11-670x450.jpg" alt="">
          <img class="youtubeIcon" src="/img/icon-youtube-play.png" alt="">
          <img class="cloud" src="/assets/svg-0.svg" alt="">
          <img class="point" src="/img/maxcoach-shape-05.png" alt="">
          <img class="point-square" src="/img/maxcoach-shape-07.png" alt="">
        </div>
      </div>
      <div class="right-section">
        <span class="subtitle">HOW WE WORK</span>
        <h2><strong>Upgrade Your Skills</strong> <span class="title">Upgrade Your Life</span></h2>
        <p>Opening up more opportunities in front of you to get the ticket to more enjoyable door in life. Getting equipped with new skills for new sets of insights into your career. MaxCoach accompany learners in every stage of learning.</p>
        <a href="#">Download free guidebook <i class="fa-solid fa-arrow-right"></i></a>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.background{
  padding-top: 200px;
  .main-container{
    max-width: 1200px;
    margin: auto;
    display: flex;
    gap: 150px;
    .left-section{
      .img-container{
        position: relative;
        cursor: pointer;
        .youtubeIcon{
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%,-50%);
          cursor: pointer;
        }
        .cloud{
          position: absolute;
          top: -100px;
          left: -80px;
          z-index: -1;
          filter: invert(98%) sepia(22%) saturate(5365%) hue-rotate(180deg) brightness(109%) contrast(108%);
        }
        .point{
          position: absolute;
          top: 50px;
          left: -100px;
          z-index: -1;
        }
        .point-square {
          position: absolute;
          right: 0;
          bottom: -100px;
          right: -30px;
          z-index: -1;
        }
      }
    }
    .right-section{
      padding-top: 35px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      position: relative;
      .subtitle::before{
        content: '';
          width: 60px;
          height: 60px;
          position: absolute;
          border: 10px solid #ecc5ab;
          border-radius: 50%;
          top: -50px;
      }
      h2{
        font-size: 3em;
      }
      .subtitle{
        color: gray;
      }
      .title{
        color: #20ad96;
        font-weight: 400;
      }
      p{
        color: gray;
      }
      a{
        color: black;
      }
    }
  }
}

</style>