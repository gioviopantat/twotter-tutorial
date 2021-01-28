<template>
  <div class="root">
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Indie+Flower&display=swap"
      rel="stylesheet"
    />
    <v-btn class="floating-button1" elevation="5" fab></v-btn>
    <form class="loginForm">
      <kinesis-container class="h1-container">
        <kinesis-element :strength="20">
          <h1 @mouseover="hover" @mouseleave="leave">
            {{ h1Text }}<br />Give Me Your Information
          </h1>
        </kinesis-element>
      </kinesis-container>
      <v-text-field
        v-model="username"
        :error-messages="usernameErrors"
        :counter="20"
        label="Username"
        required
        @input="$v.username.$touch()"
        @blur="$v.username.$touch()"
      ></v-text-field>
      <v-text-field
        v-model="email"
        :error-messages="emailErrors"
        label="E-mail"
        required
        @input="$v.email.$touch()"
        @blur="$v.email.$touch()"
      ></v-text-field>
      <v-text-field
        label="Password"
        type="password"
        required
        @input="$v.email.$touch()"
        @blur="$v.email.$touch()"
      ></v-text-field>
      <div class="button-submit-clear">
        <v-btn class="mr-4" @click="submit">
          submit
        </v-btn>
        <v-btn @click="clear">
          clear
        </v-btn>
      </div>
    </form>
  </div>
</template>
<script>
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";

export default {
  mixins: [validationMixin],

  validations: {
    username: { required, maxLength: maxLength(10) },
    email: { required, email },
    select: { required },
    checkbox: {
      checked(val) {
        return val;
      },
    },
  },
  name: "loginPage",

  data: () => ({
    username: "",
    email: "",
    h1Text: "WHAT UP PAL",
  }),
  computed: {
    usernameErrors() {
      const errors = [];
      if (!this.$v.username.$dirty) return errors;
      !this.$v.username.maxLength &&
        errors.push("Username must be at most 20 characters long");
      !this.$v.username.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    },
  },

  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.username = "";
      this.email = "";
    },
    hover() {
      this.h1Text = "LEAVE ME ALONE";
    },
    leave() {
      this.h1Text = "WHAT UP PAL";
    },
    click1() {
      console.log("clicked");
    },
  },
};
</script>

<style scoped>
::v-deep .v-text-field {
  width: 80%;
  margin-left: 10%;
  margin-top: 40px;
}
.loginForm {
  width: 30%;
  height: 65%;
  background: white;
  text-align: center;
  padding-top: 50px;
  border-radius: 10px;
  margin: 0 auto;
  box-shadow: 3px 3px 5px 6px #cccccc;
  font-family: "Indie Flower", cursive;
}
.button-submit-clear {
  margin-top: 10px;
}
.floating-button1 {
  margin-left: 5px;
  margin-bottom: 5px;
}
.pic1 {
  width: 20%;
  height: 20%;
}
</style>
