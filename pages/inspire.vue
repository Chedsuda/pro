<template>
  <div>
    <!-- Menu --><NuxtLink to="/index">
      <v-btn icon>
        <v-icon>mdi-cart</v-icon>
      </v-btn>
    </NuxtLink>
    <v-text-field
      v-model="search"
      append-icon="mdi-magnify"
      label="Search"
      single-line
      hide-details
    ></v-text-field>
    <v-data-table
      :search="search"
      :headers="this.$store.state.headers"
      :items="this.$store.state.data"
      :items-per-page="5"
      class="elevation-1"
    />
  </div>
</template>
<script>
export default {
  data() {
    return {
      search: '',
    }
  },
}
</script>
