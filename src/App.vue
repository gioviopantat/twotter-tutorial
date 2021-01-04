<template>
  <v-app>
    <v-main>
      <!-- <HelloWorld/>
      <background/>
      <pagination/> -->
      <Parallax/>
    </v-main>
  </v-app>
</template>

<script>
import Parallax from './components/Parallax.vue';
import Vue from 'vue'
import VueKinesis from 'vue-kinesis'

Vue.use(VueKinesis)
// import HelloWorld from './components/HelloWorld';
// import pagination from './components/pagination';
// import background from './components/background';

export default {
  name: 'App',

  components: {
    Parallax
    // HelloWorld,
    // pagination,
    // background
  },

  data: () => ({
    // v0: true,
  })
};
</script>
