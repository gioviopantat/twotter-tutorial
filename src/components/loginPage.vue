<template>
  <div class="root">
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Indie+Flower&display=swap"
      rel="stylesheet"
    />
    <form class="loginForm">
      <kinesis-container class="h1-container">
        <kinesis-element :strength="20">
          <h1>WHAT UP PAL</h1>
        </kinesis-element>
      </kinesis-container>
      <v-text-field
        v-model="name"
        :error-messages="nameErrors"
        :counter="20"
        label="Name"
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
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
    name: { required, maxLength: maxLength(10) },
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
    name: "",
    email: "",
  }),
  computed: {
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 20 characters long");
      !this.$v.name.required && errors.push("Name is required.");
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
      this.name = "";
      this.email = "";
    },
  },
};
</script>

<style scoped>
::v-deep .v-text-field {
  width: 400px;
  margin-left: 10%;
  margin-top: 40px;
}
.loginForm {
  width: 500px;
  height: 600px;
  background: white;
  text-align: center;
  padding-top: 50px;
  border-radius: 10px;
  margin: 0 auto;
  box-shadow: 3px 3px 5px 6px #cccccc;
  font-family: "Indie Flower", cursive;
}
.button-submit-clear {
  margin-top: 30px;
}
</style>
