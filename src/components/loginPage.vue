<template>
    <v-app class="root" style="backgroundColor: #b8b7b7">
        <div class="loginForm">
            <link rel="preconnect" href="https://fonts.gstatic.com">
            <link href="https://fonts.googleapis.com/css2?family=Roboto+Mono&display=swap" rel="stylesheet">
            <h1 class="header1">Login</h1>
            <v-text-field
            class="usernameBlock"
            label="Outlined"
            placeholder="Username"
            outlined
            ></v-text-field>
            <br/>
            <v-divider class="login-devider"/>
            <v-text-field
            class="passwordBlock"
            label="Outlined"
            placeholder="Password"
            outlined
            ></v-text-field>
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
        background: white);
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
        font-family: 'Roboto Mono', monospace;
    }
    input {
        margin-top: 5px;
    }
    .login-devider {
        width: auto;
        margin-top: 30px;
    }
</style>