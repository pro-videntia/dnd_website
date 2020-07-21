<template>
  <v-app>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="10">
          <v-img src="/DnD_Login_Logo.png"></v-img>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="12" md="4">
          <v-card class="mx-auto mt-6" width="100%">
            <v-card-text>
              <h4 class="primary--text text-center text-uppercase">Login</h4>
              <v-form>
                <v-text-field
                  label="Email"
                  v-model="user.email"
                  prepend-icon="mdi-email"
                />
                <v-text-field
                  :type="showPassword ? 'text' : 'password'"
                  label="Password"
                  v-model="user.password"
                  prepend-icon="mdi-account-lock"
                  :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                  @click:append="showPassword = !showPassword"
                />
              </v-form>
            </v-card-text>
            
            <v-card-actions class="justify-center">
              <v-btn
                x-large
                color="primary"
                width="75%"
                type="submit"
                class="mb-4"
                @click="loginUser"
                >Login</v-btn
              >
            </v-card-actions>
          </v-card>
          <div class="mt-10">
            <h5 class="grey--text text-center text-uppercase">
              <n-link to="/signup">
                Create an account
              </n-link>
            </h5>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
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
    },
  },
};
</script>

<style lang="scss" scoped></style>
