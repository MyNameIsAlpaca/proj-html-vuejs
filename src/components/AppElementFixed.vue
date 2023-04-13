<script>
import {store} from "../store.js";

export default {
  name: "AppElementFixed",
    data() {
        return {
            store,
        };
    }, 

    components: {  },
}

</script>

<template>
  <div class="main-container">
    <i class="fa-solid fa-pen-ruler"></i>
    <i class="fa-solid fa-life-ring"></i>
    <i class="fa-solid fa-book"></i>
    <i class="fa-solid fa-cart-shopping"></i>
  </div>
</template>

<style scoped lang="scss">
.main-container{
  position: fixed;
  right: 0;
  background-color: white;
  display: flex;
  flex-direction: column;
  gap: 10px;
  border-radius: 10px 0 0px 10px;
  overflow: hidden;
  text-align: center;
  z-index: 5;
  border: 1px dotted rgba(211, 211, 211, 0.534);
  .fa-solid{
    padding: 10px;
  }
  .fa-solid:hover{
    background-color: lightblue;
    cursor: pointer;
  }
}

</style>