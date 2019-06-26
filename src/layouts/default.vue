<template>
  <v-app>
    <the-toolber></the-toolber>
    <v-content>
      <nuxt />
    </v-content>
    <the-footer></the-footer>
  </v-app>
</template>

<script>
import TheFooter from '~/components/organisms/TheFooter'
import TheToolber from '~/components/organisms/TheToolber'
export default {
  components: {
    TheToolber,
    TheFooter
  }
}
</script>
<style></style>
