<template>
    <div id="app">
        <v-app id="pagination">
            <div class="text-center">
                <v-pagination
                 v-model="page"
                 :length="6"
                ></v-pagination>
            </div>
        </v-app>
    </div>
</template>

<script>
  export default {
    name: 'pagination',

    data: () => ({
      
    }),
  }
</script>
