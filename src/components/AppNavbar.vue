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
                  'Torna indietro', 'vai avanti'
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
                  'Torna indietro', 'vai avanti'
                ]
              },
              {
                name: 'Features',
                content: [
                  'Torna indietro', 'vai avanti'
                ]
              },
              {
                name: 'Blog',
                content: [
                  'Torna indietro', 'vai avanti'
                ]
              },
              {
                name: 'Shop',
                content: [
                  'Torna indietro', 'vai avanti'
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
            <a class="nav-link" href="#"> {{ link.name }} <i class="fa-solid fa-chevron-down"></i></a>
            <ul class="dropdown-menu">
              <li class="dropdownInfo" v-for="sub in link.content"><a class="dropdown-item" href="#"> {{ sub }}</a></li>
            </ul>
          </li>
        </ul>
      </nav>
    </div>
    <div class="logo">

    </div>
    <div class="rightLinks">

    </div>
  </div>
  
</template>

<style scoped lang="scss">
.container-fluid{
  max-width: 1500px;
  .leftLinks {
    .navbar {
      .linkContainer{
        display: flex;
        gap: 30px;
        list-style-type: none;
        .nav-item{
          .active{
            background-color: red;
          }
        }
        .nav-item:hover .dropdown-menu{
          display: block;
          .dropdownInfo {
            --bs-dropdown-link-active-bg: #20ad96;
          }
        }
        .nav-item:hover {
          color: #20ad96;
          border-bottom: 1px solid #20ad96;
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
          margin-top: 20px;
          border: 0;
          border-bottom: 2px solid #20ad96;
          border-radius: 0;
          --bs-dropdown-min-width: 0;
        }
      }
    }
  }
}
</style>