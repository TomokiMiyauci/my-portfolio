<template>
  <v-app>
    <the-toolber></the-toolber>
    <v-portfolio></v-portfolio>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import TheToolber from '~/components/organisms/TheToolber'
import VPortfolio from '~/components/organisms/VPortfolio'
export default {
  components: {
    TheToolber,
    VPortfolio
  }
}
</script>
<style></style>
