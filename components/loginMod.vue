<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="8" offset-md="2">
        <v-card class="mx-auto" width="100%">
          <v-card-text>
            <v-form>
              <v-text-field
                label="Email"
                v-model="user.email"
                prepend-icon="mdi-account-circle"
              />
              <v-text-field
                :type="showPassword ? 'text' : 'password'"
                label="Password"
                v-model="user.password"
                prepend-icon="mdi-lock"
                :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                @click:append="showPassword = !showPassword"
              />
            </v-form>
          </v-card-text>
          <div class="py-12"></div>
          <v-card-actions>
            <v-btn to="/signup" color="success">Register</v-btn>
            <v-spacer></v-spacer>
            <v-btn color="info" @click="loginUser">Login</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "LoginPage",
  data() {
    return {
      showPassword: false,
      user: {
        email: "",
        password: "",
      },
    };
  },
  methods: {
    loginUser() {
      console.log(this.user);
      this.user.email = "";
      this.user.password = "";
    },
  },
};
</script>

<style lang="scss" scoped></style>
