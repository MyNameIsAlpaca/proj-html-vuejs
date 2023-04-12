<script>
import {store} from "../store.js";

export default {
  name: "AppTestimonialsTop",
    data() {
        return {
            store,
            activeCard: 0,
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
      <div class="subtitles">
        TESTIMONIALS
      </div>
      <h2 class="title">Why Do People <span class="coloredTitle">*Hearts*</span> Us?</h2>
      <p>Seeking for verbals of our service quality? Find them here. Everything is transparent and straightforward for your sense of justifcation.</p>
      <a href="#">View all <i class="fa-solid fa-arrow-right"></i></a>
    </div>
    <div class="right-section">
      <div class="card-container">
        <div class="card card-top" :class="activeCard == 1 ? 'active' : ''" @click="this.activeCard = 1">
          <h5 class="card-title">The MaxCoach team works really jard to ensure high level of quality</h5>
          <p class="card-description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis optio sint odio exercitationem laudantium quasi commodi alias natus molestias deserunt soluta nesciunt officiis, iure voluptates libero dolore officia at? Nulla?</p>
          <div class="user-card">
            <img src="/img/testimonial-avata-03.jpg" alt="">
            <div class="user-info">
              <strong class="user-name">Mad Max</strong>
              <span class="user-role">/ Pony trainer </span>
            </div>
          </div>
        </div>
        <div class="card card-mid" :class="activeCard == 0 ? 'active' : ''" @click="this.activeCard = 0">
          <h5 class="card-title">Professional team of specialists and passionate mentors at reach</h5>
          <p class="card-description">I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.</p>
          <div class="user-card">
            <img src="/img/testimonial-avata-01.jpg" alt="">
            <div class="user-info">
              <strong class="user-name">MADLEY PONDOR</strong>
              <span class="user-role">/ IT Specialist</span>
            </div>
          </div>
        </div>
        <div class="card card-bot" :class="activeCard == 2 ? 'active' : ''" @click="this.activeCard = 2">
          <h5 class="card-title">The greatest satisfaction a queen can achieve</h5>
          <p class="card-description">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequuntur obcaecati quis ea iusto hic, voluptatum beatae ipsam doloremque eum, nemo magni sapiente impedit ducimus! Labore et ex aliquid architecto eligendi.</p>
          <div class="user-card">
            <img src="/img/testimonial-avata-02.jpg" alt="">
            <div class="user-info">
              <strong class="user-name">MADLEY PONDOR</strong>
              <span class="user-role">/ IT Specialist</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">

.main-container{
  padding-bottom: 1000px;
  padding-top: 200px;
  max-width: 1200px;
  margin: auto;
  display: flex;
  .left-section{
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 10px;
    .subtitles{
      color: gray;
    }
    .title{
      font-size: 3.2em;
      font-weight: 700;
    }
    .coloredTitle{
      color: #20ad96;
      font-weight: 300;
    }
    a{
      color: black;
      font-weight: 600;
    }
  }
  .right-section{
    .card-container{
      position: relative;
      
      .card.active{
        z-index: 3;
        opacity: 1;

      }
      .card-top{
        position: absolute;
        top: -180px;
      }
      .card-mid{
        position: relative;
      }
      .card-bot{
        position: absolute;
        top: 180px;
      }
      .card{
        padding: 40px;
        border: 0;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
        opacity: 0.5;
        .card-description{
          color: gray;
          font-weight: 500;
        }
        .user-card{
          display: flex;
          img{
            width: 60px;
            height: 60px;
            border-radius: 50%;
          }
          .user-info{
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding-left: 10px;
            gap: 10px;
          }
        }
      }
    }
  }
}

</style>