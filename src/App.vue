<template>
  <v-app>
    <v-main>
      <!-- <HelloWorld/>
      <pagination/> -->
      <!-- <Parallax1/> -->
      <background/>
      <index/>
    </v-main>
  </v-app>
</template>

<script>
// import Parallax1 from './components/Parallax1.vue';
import index from './components/index';
import background from './components/background';
import Vue from 'vue';
import VueKinesis from 'vue-kinesis';

Vue.use(VueKinesis)
// import HelloWorld from './components/HelloWorld';
// import pagination from './components/pagination';
// import background from './components/background';

export default {
  name: 'App',

  components: {
    // Parallax1,
    // HelloWorld,
    // pagination,
    background,
    index
  },

  data: () => ({
    // v0: true,
  })
};
</script>
