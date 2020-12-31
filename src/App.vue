<template>
  <v-app>
    <v-main>
      <HelloWorld/>
      <pagination/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import pagination from './components/pagination';

export default {
  name: 'App',

  components: {
    HelloWorld,
    pagination
  },

  data: () => ({
    v0: true,
  })
};
</script>
