<template>
  <v-row align="center" justify="center">
    <v-col cols="12" sm="8" md="4" align="center">
      <v-card class="elevation-4 text-left">
        <v-card-title class="fancy-title align-center justify-center">
          My Trello App
        </v-card-title>
        <v-card-text>
          <v-form>
            <!-- FORM START -->
            <v-text-field
              label="Login"
              name="login"
              prepend-icon="mdi-account"
              type="text"
              v-model="auth.email"
            >
            </v-text-field>
            <v-text-field
              label="Password"
              name="password"
              prepend-icon="mdi-lock"
              type="password"
              v-model="auth.password"
            >
            </v-text-field>
          </v-form>
        </v-card-text>
        <v-card-actions class="text-center">
          <v-btn class="login-button" @click="login" depressed large
            >Login</v-btn
          >
        </v-card-actions>
      </v-card>
      <v-snackbar :timeout="4000" v-model="snackbar" absolute bottom center>
        {{ snackbarText }}
      </v-snackbar>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "SignIn",
  data() {
    return {
      snackbar: false,
      snackbarText: "No error message",
      auth: {
        email: "",
        password: ""
      }
    };
  },
  methods: {
    login() {
      // login with firebase later
    }
  }
};
</script>

<style lang="scss" scoped></style>
