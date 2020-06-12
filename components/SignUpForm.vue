<template>
  <v-app>
    <v-card width="400" class="mx-auto">
      <v-card-text>
        <v-form>
          <v-text-field
            label="First Name"
            prepend-icon="mdi-account-circle"
            v-model="firstName"
            :rules="firstNameRules"
            required
          ></v-text-field>
          <v-text-field
            label="Last Name"
            prepend-icon="mdi-account-circle"
            v-model="lastName"
            :rules="lastNameRules"
            required
          ></v-text-field>
          <v-text-field
            label="Email Address"
            prepend-icon="mdi-email"
            type="email"
            v-model="email"
            :rules="emailRules"
            required
          ></v-text-field>
          <v-text-field
            :type="showPassword ? 'text' : 'password'"
            label="Password"
            prepend-icon="mdi-account-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
            v-model="password"
            :rules="passwordRules"
          ></v-text-field>
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-btn color="success" type="submit">Signup</v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
export default {
  name: "SignUpForm",
  data() {
    return {
      showPassword: false,
      firstName: "",
      firstNameRules: [
        (v) => !!v || "First name is required",
        (v) => (v && v.length <= 10) || "Name must be less than 10 characters",
      ],
      lastName: "",
      lastNameRules: [
        (v) => !!v || "Last name is required",
        (v) =>
          (v && v.length <= 10) || "Last name must be less than 10 characters",
      ],
      email: "",
      emailRules: [
        (v) => !!v || "E-mail is required",
        (v) => /.+@.+\..+/.test(v) || "E-mail must be valid",
      ],
      password: "",
      passwordRules: [(v) => !!v || "Password is required"],
    };
  },
};
</script>
