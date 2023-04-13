<script>
import {store} from "../store.js";

export default {
  name: "AppFooter",
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
      <span class="title">Address</span>
      <ul>
        <li>382 NE 191 St # 87394 Miami, FL 33179-3899</li>
        <li>+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)</li>
        <li>support@maxcoach.com</li>
      </ul>
      <div class="social">
        <i class="fa-brands fa-square-facebook"></i>
        <i class="fa-brands fa-twitter"></i>
        <i class="fa-brands fa-instagram"></i>
        <i class="fa-brands fa-linkedin"></i>
      </div>
    </div>
    <div class="right-section">
      <div class="explore">
        <div class="title">Explore</div>
        <ul>
          <li>Start here</li>
          <li>Blog</li>
          <li>About us</li>
        </ul>
      </div>
      <div class="unkown">
        <ul>
          <li>Success story</li>
          <li>Courses</li>
          <li>Contact us</li>
        </ul>
      </div>
      <div class="information">
        <div class="title">Information</div>
        <ul>
          <li>Membership</li>
          <li>Purchase guide</li>
          <li>Privacy policy</li>
          <li>Terms of service</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="copyright">
    <span>&copy; 2020 Maxcoach. All Rights Reserved</span>
  </div>
  </div>
</template>

<style scoped lang="scss">

.background{
  background-color: #171621;
  .main-container{
    color: white;
    padding-top: 100px;
    max-width: 1200px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    .left-section{
      display: flex;
      flex-direction: column;
      gap: 15px;
      .title{
        font-size: 1.3em;
        font-weight: 600;
      }
      ul{
        list-style-type: none;
        padding: 0;
        display: flex;
        flex-direction: column;
        gap: 10px;
        color: #ababab;
      }
      .social{
        color: #ababab;
        font-size: 1.5em;
        display: flex;
        gap: 30px;
        .fa-brands:hover{
          cursor: pointer;
          color: #20AD96;
        }
      }
    }
    .right-section{
      display: flex;
      gap: 100px;
      .unkown{
        padding-top: 45px;
      }
      .title{
        padding-bottom: 10px;
        font-size: 1.3em;
        font-weight: 600;
      }
      ul{
        list-style-type: none;
        padding: 0;
        display: flex;
        flex-direction: column;
        gap: 10px;
        color: #ababab;
        li:hover{
          cursor: pointer;
          color: #20AD96;
        }
      }
    }
  }
  .copyright{
    color: #ababab;
    padding-top: 50px;
    padding-bottom: 50px;
    text-align: center;
  }
}


</style>