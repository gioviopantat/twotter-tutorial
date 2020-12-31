<template>
  <v-app>
    <v-main>
      <HelloWorld/>
      <background/>
      <pagination/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import pagination from './components/pagination';
import background from './components/background';

export default {
  name: 'App',

  components: {
    HelloWorld,
    pagination,
    background
  },

  data: () => ({
    v0: true,
  })
};
</script>
