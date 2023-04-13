<script>

import AppBlog from "./components/AppBlog.vue";
import AppBotInfo from "./components/AppBotInfo.vue";
import AppJumbo from "./components/AppJumbo.vue";
import AppLatest from "./components/AppLatest.vue";
import AppNavbar from "./components/AppNavbar.vue";
import AppNewsLetter from "./components/AppNewsLetter.vue";
import AppTestimonialsBot from "./components/AppTestimonialsBot.vue";
import AppTestimonialsTop from "./components/AppTestimonialsTop.vue";
import AppTopInfo from "./components/AppTopInfo.vue";
import {store} from "./store.js";

import axios from "axios";

export default {
  data() {
    return {
      store,
    }
  },

  components: {
    AppNavbar,
    AppJumbo,
    AppTopInfo,
    AppBotInfo,
    AppLatest,
    AppTestimonialsTop,
    AppTestimonialsBot,
    AppBlog,
    AppNewsLetter
},

  methods: {
  },

}
</script>

<template>
  <AppNavbar></AppNavbar>
  <AppJumbo></AppJumbo>
  <AppTopInfo></AppTopInfo>
  <AppBotInfo></AppBotInfo>
  <AppLatest></AppLatest>
  <AppTestimonialsTop></AppTestimonialsTop>
  <AppTestimonialsBot></AppTestimonialsBot>
  <AppBlog></AppBlog>
  <AppNewsLetter></AppNewsLetter>
</template>

<style lang="scss">

</style>
