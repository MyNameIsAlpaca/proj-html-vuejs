<script>
import {store} from "../store.js";

export default {
  name: "AppNavbar",
    data() {
        return {
            store,
            navLinks: [
              {
                name: 'Home',
                content: [
                ]
              },
              {
                name: 'Pages',
                content: [
                  'Start Here', 'Success Story', 'About me', 'About Us 01', 'About Us 02', 'About Us 03', 'Contact me', 'Contact Us', 'Purchase Guide', 'Privacy Policy', 'Terms of Service'
                ]
              },
              {
                name: 'Courses',
                content: [
                  'Cooking class', 'Coding class', 'Running course'
                ]
              },
              {
                name: 'Features',
                content: [
                  'Sponsor', 'Free trial'
                ]
              },
              {
                name: 'Blog',
                content: [
                  'Cooking blog', 'Coding blog', 'Gaming blog', 'Movie blog'
                ]
              },
              {
                name: 'Shop',
                content: [
                  'T-shirt Shop', 'Hat Shop', 'Shoes Shop'
                ]
              },
            ]
        };
    }, 

    components: {  },
}

</script>

<template>

  <div class="container-fluid">
    <div class="leftLinks">
      <nav class="navbar">
        <ul class="linkContainer">
          <li v-for="link in navLinks" class="nav-item dropdown">
            <a class="nav-link" href="#"> {{ link.name }} <i v-show="link.name != 'Home'" class="fa-solid fa-chevron-down"></i></a>
            <ul class="dropdown-menu">
              <li class="dropdownInfo" v-for="sub in link.content"><a class="dropdown-item" href="#"> {{ sub }}</a></li>
            </ul>
          </li>
        </ul>
      </nav>
    </div>
    <div class="logo">
      <img src="/img/dark-logo.png" alt="logo max coach">
    </div>
    <div class="rightLinks">
      <i class="fa-sharp fa-solid fa-cart-shopping"><div class="itemCart">0</div></i>
      <i class="fa-regular fa-user"></i>
      <div class="input-box">
        <input type="text" class="form-control" placeholder="Search...">
        <i class="fa fa-search"></i>                    
      </div>
    </div>
  </div>
  
</template>

<style scoped lang="scss">
.container-fluid{
  max-width: 1500px;
  display: flex;
  height: 70px;
  align-items: center;
  justify-content: space-between;
  .leftLinks {
    .navbar {
      .linkContainer{
        display: flex;
        gap: 30px;
        list-style-type: none;
        .nav-item:hover:after {
          content: '';
          width: 100%;
          height: 1px;
          background-color: #20ad96;
          position: absolute;
        }
        .nav-item:hover{
          color: #20ad96;
        }
        .nav-item:hover .dropdown-menu{
          display: block;
          .dropdownInfo {
            --bs-dropdown-link-active-bg: #20ad96;
          }
        }
        .nav-link {
          display: flex;
          align-items: center;
          gap: 5px;
        }
        .fa-chevron-down {
          font-size: 0.5em;
        }
        .dropdown-menu {
          padding: 0;
          padding-top: 30px;
          margin-top: 1px;
          border: 0;
          border-bottom: 2px solid #20ad96;
          border-radius: 0;
          --bs-dropdown-min-width: 0;
        }
      }
    }
  }
  .logo{
    height: 100%;
    display: flex;
    align-items: center;
    img{
      height: 40%;
    }
  }

  .rightLinks{
    display: flex;
    align-items: center;
    gap: 20px;
    .fa-user{
      border: 1px solid black;
      border-radius: 25px;
      padding: 3px;
      font-size: 0.5em;
    }
    .fa-cart-shopping{
      position: relative;
      .itemCart{
        position: absolute;
        top: -10px;
        right: -5px;
        font-size: 0.5em;
        padding: 3px 4px;
        border-radius: 25px;
        background-color: #20ad96;
        color: white;
        text-align: center;
      }
    }
    .input-box{
    position: relative;

      i {
      position: absolute;
      right: 13px;
      top:12px;
      color: #20ad96;
      }
    }

    input{
      background-color: #f5f5f5;
    }

    input:focus{
      border-color: #20ad96;
      box-shadow: 0 1px 1px rgba(0, 0, 0, 0.075) inset, 0 0 8px #20ad96;
      outline: 0 none;
    }

  }

}
</style>