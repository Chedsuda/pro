<template>
  <v-app dark>
    <v-app-bar
      dark
      prominent
      src="https://www.centralworld.co.th/wp-content/uploads/2019/08/shutterstock_69380449-2.jpg"
      :clipped-left="clipped"
      fixed
      app
    >
      <v-toolbar-title v-text="title" /><!-- Logout -->
      <v-spacer /><NuxtLink to="/log">
        <v-btn icon>
          <v-icon>mdi-export</v-icon>
        </v-btn></NuxtLink
      >
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Coffee Shop',
    }
  },
}
</script>
