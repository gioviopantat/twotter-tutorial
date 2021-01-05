<template>
    <v-app class="root">
        <img class="car" src="../../static/car2.png"/>
    </v-app>
</template>

<script>
export default {
    name: 'car',
    data: () => ({

    })
}
</script>

<style scoped>
    .car {
        max-width: 800px;
        max-height: 600px;
        position: absolute;
        top: 175px;
        left: 500px;
    }
</style>