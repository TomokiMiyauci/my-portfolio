<template>
  <v-toolbar color="red" dark>
    <v-toolbar-title>
      <v-avatar size="30px">
        <v-img
          :src="require('~/assets/logo/my-portfolio.png')"
          alt="avatar"
        ></v-img>
      </v-avatar>
      <span>My Portfolio</span>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn flat to="/">Home</v-btn>
      <v-btn flat to="/carrer">Carrer</v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {}
</script>

<style></style>
