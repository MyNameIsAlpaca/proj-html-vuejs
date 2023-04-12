<script>
import {store} from "../store.js";

export default {
  name: "AppJumbo",
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
    <div class="info">
      <h2>Commence Business</h2>
      <h1>Distant Mentoring Program</h1>
      <button>Download free guidebook <i class="fa-solid fa-arrow-right"></i></button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.background{
  background-image: url(/img/home-3-hero-bg.jpg);
  height: 636px;
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  .info{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    
    h1{
      font-size: 3.5em;
      text-shadow: 2px 2px rgba(0, 0, 0, 0.514);
      padding-bottom: 15px;
    }
    h2{
      font-size: 2.5em;
      text-shadow: 2px 2px rgba(0, 0, 0, 0.514);
    }
    button{
      padding: 15px 30px;
      border-radius: 10px;
      border: 0;
      color: #20AD96;
      font-weight: bold;
      display: flex;
      align-items: center;
      gap: 20px;
    }
  }
}
</style>