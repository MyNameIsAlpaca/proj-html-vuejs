<script>
import {store} from "../store.js";

export default {
  name: "AppBlog",
    data() {
        return {
            store,
            blogList: [
              {
                image: '/img/artist-blog-03-480x325.jpeg',
                type: 'ARTIST',
                name: 'Brush Strokes Energize Trees in Paintings',
                date: 'May 15, 2020',
                views: 688,
              },
              {
                image: '/img/artist-blog-01-480x325.jpg',
                type: 'ARTIST',
                name: 'Pocket-Sized Notebooks Hold Miniature Paintings',
                date: 'May 15, 2020',
                views: 603,
              },
              {
                image: '/img/artist-blog-02-480x325.jpg',
                type: 'ARTIST',
                name: 'Connection Between Self-Portraits and Identity',
                date: 'May 15, 2020',
                views: 397,
              },
            ]
        };
    }, 

    components: {  },
}

</script>

<template>
  <div class="background">
    <div class="main-container">
      <span>READ FOR MORE JOYMENT</span>
      <h2 class="title">Latest From <span class="titleColored">Our Blogs</span></h2>
      <div class="card-container">
        <div v-for="card in blogList" class="card">
          <img :src="card.image" alt="">
          <span>{{card.type}}</span>
          <h5>{{ card.name }}</h5>
          <div class="info">
            <div class="date">
              <i class="fa-regular fa-calendar"></i> {{ card.date }}
            </div>
            <div class="views">
              <i class="fa-regular fa-eye"></i> {{ card.views }} views
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.background{
  background-color: #f8f8f8;
  .main-container{
    max-width: 1200px;
    margin: auto;
    margin-top: 150px;
    padding-top: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    padding-bottom: 100px;
    span{
      color: gray;
    }
    .title{
      font-size: 3.5em;
      .titleColored{
        color: #20ad96;
        font-weight: 300;
      }
    }
    .card-container{
      width: 100%;
      display: flex;
      justify-content: space-between;
      .card:hover{
        padding: 5px;
      }
      .card{
        max-width: calc(100% / 3 - 20px);
        border: 0;
        display: flex;
        flex-direction: column;
        gap: 10px;
        background-color: #f8f8f8;
        cursor: pointer;
        .info{
          display: flex;
          gap: 30px;
          font-size: 0.9em;
          color: gray;
        }
      }
    }
  }

}
</style>