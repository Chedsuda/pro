<template>
  <v-row justify="center">
    <br />
    <v-col cols="11" sm="6" md="8" lg="4">
      <v-card ref="form" width="350">
        <v-img
          height="350px"
          src="https://i.pinimg.com/564x/8b/83/c0/8b83c0b67104d8da4b7bd9d4496b0fb7.jpg"
        >
          <v-card-text
            ><br />
            <p class="ti">Login</p>
            <br />
            <v-text-field class="material" label="ID" required></v-text-field>
            <v-text-field
              class="material"
              :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required]"
              :type="show1 ? 'text' : 'password'"
              label="Password"
              @click:append="show1 = !show1"
            ></v-text-field>
          </v-card-text>
          <v-card-actions>
            <NuxtLink to="/register">
              <v-btn color="error" text @click="submit"> Register </v-btn>
            </NuxtLink>
            <v-spacer></v-spacer>
            <NuxtLink to="/order">
              <v-btn color="primary" text @click="submit">
                Login
              </v-btn></NuxtLink
            >
          </v-card-actions>
        </v-img>
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data() {
    return {
      show1: false,
      password: 'Password',
      rules: {
        required: (value) => !!value || 'This field is required',
      },
    }
  },
}
</script>
<style>
@import url(https://fonts.googleapis.com/css2?family=Abel&display=swap);
.ti {
  font-family: 'Abel', sans-serif;
  font-size: 30px;
  text-align: center;
}
.material {
  font-family: 'Abel', sans-serif;
  color: black;
}
</style>
