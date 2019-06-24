<template>
  <div>
    <v-experience></v-experience>
    <v-products></v-products>
  </div>
</template>

<script>
import VExperience from '~/components/molecules/VExperience'
import VProducts from '~/components/molecules/VProducts'
export default {
  layout: 'index',
  components: {
    VExperience,
    VProducts
  }
}
</script>

<style></style>
