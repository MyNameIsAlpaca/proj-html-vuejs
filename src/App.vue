<script>

import AppJumbo from "./components/AppJumbo.vue";
import AppNavbar from "./components/AppNavbar.vue";
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
    AppJumbo
},

  methods: {
  },

}
</script>

<template>
  <AppNavbar></AppNavbar>
  <AppJumbo></AppJumbo>
</template>

<style scoped lang="scss">

</style>
