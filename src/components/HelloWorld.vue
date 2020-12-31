<template>
  <!-- <div id="app">
    <v-app id="inspire">
      <v-bottom-navigation
        :value="value"
        color="teal"
        grow
      >
        <v-btn>
          <span>Recents</span>
    
          <v-icon>mdi-history</v-icon>
        </v-btn>
    
        <v-btn>
          <span>Favorites</span>
    
          <v-icon>mdi-heart</v-icon>
        </v-btn>
    
        <v-btn>
          <span>Nearby</span>
    
          <v-icon>mdi-map-marker</v-icon>
        </v-btn>
      </v-bottom-navigation>
    </v-app>
  </div> -->
  <div id="app">
  <v-app id="inspire">
    <div>
      <v-checkbox
        v-model="v0"
        label="Visible"
      ></v-checkbox>
      <v-banner
        v-model="v0"
        single-line
        transition="slide-y-transition"
      >
        No Internet connection
        <template v-slot:actions="{ dismiss }">
          <v-btn
            text
            color="primary"
            @click="dismiss"
          >
            Dismiss
          </v-btn>
          <v-btn
            text
            color="primary"
          >
            Retry
          </v-btn>
        </template>
      </v-banner>
    </div>
  </v-app>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      
    }),
  }
</script>
