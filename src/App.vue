<script>

import AppJumbo from "./components/AppJumbo.vue";
import AppNavbar from "./components/AppNavbar.vue";
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
    AppTopInfo
},

  methods: {
  },

}
</script>

<template>
  <AppNavbar></AppNavbar>
  <AppJumbo></AppJumbo>
  <AppTopInfo></AppTopInfo>
</template>

<style scoped lang="scss">

</style>
