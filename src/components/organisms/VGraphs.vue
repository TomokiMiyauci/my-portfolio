<template>
  <v-container fluid grid-list-lg>
    <v-layout row wrap justify-space-around>
      <v-flex xs12 sm6 md4 xl4>
        <v-age></v-age>
      </v-flex>
      <v-flex xs12 sm6 md4 xl4>
        <v-proportion></v-proportion>
      </v-flex>
      <v-flex xs12 sm6 md4 xl4>
        <v-programing></v-programing>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import VPrograming from '~/components/organisms/VPrograming'
import VAge from '~/components/organisms/VAge'
import VProportion from '~/components/organisms/VProportion'

export default {
  components: {
    VProportion,
    VAge,
    VPrograming
  }
}
</script>
