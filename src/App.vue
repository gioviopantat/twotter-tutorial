<template>
  <v-app>
    <v-main>
      <!-- <HelloWorld/>
      <pagination/> -->
      <!-- <Parallax1/> -->
      <!-- <background/> -->
      <!-- <index/> -->
      <!-- <car/> -->
      <loginPage/>
    </v-main>
  </v-app>
</template>

<script>
// import Parallax1 from './components/Parallax1.vue';
import Vue from 'vue';
import VueKinesis from 'vue-kinesis';
import loginPage from './components/loginPage.vue';
// import car from './components/car';

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
    // background,
    // car,
    // index,
    loginPage
  },

  data: () => ({

  })
};
</script>
