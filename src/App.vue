<script>

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
    AppNavbar
},

  methods: {
  },

}
</script>

<template>
  <AppNavbar></AppNavbar>
</template>

<style scoped lang="scss">

</style>
