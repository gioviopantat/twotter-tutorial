<template>
    <div id="app">
        <v-app id="background">
            <v-parallax src="../../static/background.jpg"></v-parallax>
        </v-app>
    </div>
</template>

<script>
  export default {
    name: 'background',

    data: () => ({
      
    }),
  }
</script>

<style scoped>
  .background {
    display: flex;
    position: absolute;
  }
</style>