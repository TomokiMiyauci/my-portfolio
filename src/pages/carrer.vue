<template>
  <div>
    <v-graphs></v-graphs>
    <v-container grid-list-xs>
      <v-career></v-career>
    </v-container>
    <v-do-i-do></v-do-i-do>
  </div>
</template>

<script>
import VGraphs from '~/components/organisms/VGraphs'
import VDoIDo from '~/components/organisms/VDoIDo'
import VCareer from '~/components/organisms/VCareer'

export default {
  components: {
    VCareer,
    VDoIDo,
    VGraphs
  }
}
</script>
