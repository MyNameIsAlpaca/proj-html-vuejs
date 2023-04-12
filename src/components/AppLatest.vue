<script>
import {store} from "../store.js";

export default {
  name: "AppLatest",
    data() {
        return {
            store,
            cardList: [
              {
                image: '/img/course-02-480x298.jpg',
                price: '40.00',
                title: 'Learning to Write as a Professional Author',
                lessons: 20,
                students: 50,
              },
              {
                image: '/img/stock-full-hd-03-480x298.jpg',
                price: '0.00',
                title: 'Customer-centric Info-Tech Strategies',
                lessons: 24,
                students: 769,
              },
              {
                image: '/img/stock-full-hd-04-480x298.jpg',
                price: '19.00',
                title: 'Open Programming Courses for Everyone: Python',
                lessons: 17,
                students: 62,
              },
              {
                image: '/img/redd-f-5U_28ojjgms-unsplash.jpg',
                price: '0.00',
                title: 'Group meeting and raise social skill',
                lessons: 10,
                students: 32,
              },
              {
                image: '/img/campaign-creators-gMsnXqILjp4-unsplash.jpg',
                price: '20.00',
                title: 'Open Programming Courses for Everyone: Javascript',
                lessons: 12,
                students: 52,
              },
            ],
            activeIndex: 0,
          };
        }, 


    components: {  },

    methods: {

      showCard(index) {

        if(this.activeIndex == 0) {

          if(this.activeIndex == index || this.activeIndex + 1 == index || this.activeIndex + 2 == index) {
            return true
          } else {
            return false
          }
        } else if (this.activeIndex == this.cardList.length - 1) {
          if(this.activeIndex == index|| this.activeIndex - 1 == index || this.activeIndex - 2 == index) {
            return true
          } else {
            return false
          }
        } else {
          if(this.activeIndex == index || this.activeIndex + 1 == index || this.activeIndex - 1 == index){

          return true

        } else {
          return false
        }
        }
      },

    },
}

</script>

<template>
  <div class="background">
    <div class="main-container">
      <div class="title">
        <span class="subtitle">JOIN MAXCOACH AT BEST</span>
        <h2>Latest Online <span class="coloredTitle">Courses</span></h2>
      </div>
      <div class="card-section">
        <div v-for="(card, index) in cardList" class="card" v-show="showCard(index)" @click="this.activeIndex = index" :class="this.activeIndex == index ? 'active' : ''">
          <div class="img-container">
            <img :src="card.image" alt="">
          </div>
          <div v-if="card.price == '0.00'" class="bookmark"><span style="color:white;position: relative;top: -15px;text-align: center;right: -10px;">Free</span></div>
          <div class="main-info">
            <span class="price">$ {{ card.price }}</span>
            <span class="titleCourse">{{ card.title }}</span>
            <div class="info">
              <span class="lessons"><i class="fa-regular fa-file-lines"></i> {{ card.lessons }} Lessons</span>
              <span class="students"><i class="fa-regular fa-user"></i> {{ card.students }} Students</span>
            </div>
          </div>
        </div>
      </div>
      <div class="dot-container">
        <div v-for="(dot, index) in cardList" class="dot" @click="this.activeIndex = index" :class="this.activeIndex == index ? 'activeDot' : ''"></div>
      </div>
      <div class="last-section">
        <span>Control your personal preference settings to get notified about appropriate courses. <a href="#">View all courses <i class="fa-solid fa-arrow-right"></i></a></span>
      </div>
    </div>
    <img class="wave" src="/assets/svg-1.svg" alt="">
  </div>
</template>

<style scoped lang="scss">
.background{
  background: rgb(255,255,255);
  background: linear-gradient(180deg, rgba(255,255,255,1) 0%, #f5f5f5 100%);
  .main-container{
    max-width: 1200px;
    margin: auto;
    padding-top: 200px;
    display: flex;
    flex-direction: column;
    gap: 40px;
    .title{
      display: flex;
      flex-direction: column;
      align-items: center;
      .subtitle{
        color: gray;
        font-size: 0.8em;
        font-weight: 600;
      }
      h2{
        font-size: 2.6em;
        .coloredTitle{
          color: #20ad96;
        }
      }
    }
    .card-section{
      display: flex;
      gap: 20px;
      justify-content: space-between;
      overflow: hidden;
      height: 500px;
      .card.active{
        background-color: lightblue;
      }
      .card{
        min-width: calc(100% / 3 - 19px);
        max-width: calc(100% / 3 - 19px);
        border-radius: 10px;
        border: 0;
        overflow: hidden;
        cursor: pointer;
        .img-container{
          max-width: 100%;
          height: 100%;
          img{
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
        
        .bookmark {
            width: 105px;
            height: 0;
            border-bottom: 20px solid #ee7455;
            border-top: 20px solid #ee7455;
            border-left: 15px solid transparent;
            float: right;
            margin-bottom: 20px;
            font-size: 17px;
            font-weight:700;
            position: absolute;
            right: 0px;
            top: 0px;
           }
        .main-info{
          display: flex;
          flex-direction: column;
          padding: 20px 40px 50px 20px;
          gap: 20px;
          .price{
            color: #20ad96;
            font-weight: bold;
            font-size: 1.3em;
          }
          .titleCourse{
            font-weight: bold;
            font-size: 1.5em;
          }
          .info{
            display: flex;
            gap: 20px;
            color: gray;
            font-size: 0.8em;
          }
        }
      }
    }
    .dot-container {
      display: flex;
      gap: 20px;
      align-self: center;
      .dot{
        background-color: lightgray;
        width: 10px;
        height: 10px;
        border-radius: 50%;
        cursor: pointer;
      }
      .dot.activeDot {
        background-color: black;
      }
    }
    .last-section {
      align-self: center;
      max-width: 500px;
      text-align: center;
      color: gray;
      padding-bottom: 50px;
      a{
        color: black;
      }
    }
  }
  .wave{
    width: 100%;
    filter: invert(95%) sepia(49%) saturate(32%) hue-rotate(300deg) brightness(99%) contrast(113%);
  }
}
</style>