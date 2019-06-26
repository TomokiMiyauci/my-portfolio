<template>
  <v-app>
    <the-toolber></the-toolber>
    <v-portfolio></v-portfolio>
    <v-content>
      <nuxt />
    </v-content>
    <the-footer></the-footer>
  </v-app>
</template>

<script>
import TheFooter from '~/components/organisms/TheFooter'
import TheToolber from '~/components/organisms/TheToolber'
import VPortfolio from '~/components/organisms/VPortfolio'
export default {
  components: {
    TheToolber,
    VPortfolio,
    TheFooter
  }
}
</script>
<style></style>
