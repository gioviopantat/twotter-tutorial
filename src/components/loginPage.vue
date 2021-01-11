<template>
    <v-app>
        <div class="loginForm">
            <h1 class="header1">Login</h1>
            <input class="usernameBlock" type="text" placeholder="Username"/>
            <br/>
            <input class="passwordBlock" type="password" placeholder="Password"/>
        </div>
    </v-app>
</template>

<script>
export default {
    name: 'loginPage',

    data: () => ({

    })
}
</script>

<style scoped>
    .loginForm {
        width: 500px;
        height: 500px;
        background: rgb(93, 92, 94);
        text-align: center;
        padding-top: 50px;
        border-radius: 10px;
        margin:0 auto;
        margin-top: 50px;
        box-shadow:3px 3px 5px 6px #cccccc;
    }
    .usernameBlock, .passwordBlock {
        width: auto;
        background-color: ghostwhite;
        border-radius: 3px;
    }
    .header1 {
        top: 20px;
        align-content: center;
    }
    input {
        margin-top: 5px;
    }
</style>