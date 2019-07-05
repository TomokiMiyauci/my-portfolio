<template>
  <v-app-bar color="red" dark>
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
      <v-btn text to="/">Home</v-btn>
      <v-btn text to="/career">Career</v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
export default {}
</script>

<style></style>
