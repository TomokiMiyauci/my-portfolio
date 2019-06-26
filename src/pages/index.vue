<template>
  <div>
    <v-portfolio></v-portfolio>
    <v-digest></v-digest>
    <v-image></v-image>
    <v-experience></v-experience>
    <v-products></v-products>
  </div>
</template>

<script>
import VPortfolio from '~/components/organisms/VPortfolio'
import VDigest from '~/components/organisms/VDigest'
import VExperience from '~/components/organisms/VExperience'
import VProducts from '~/components/organisms/VProducts'
import VImage from '~/components/organisms/VImage'
export default {
  components: {
    VDigest,
    VExperience,
    VProducts,
    VPortfolio,
    VImage
  }
}
</script>

<style></style>
