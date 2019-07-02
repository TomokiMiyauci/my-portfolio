<template>
  <div>
    <v-graphs></v-graphs>
    <v-career></v-career>
    <v-do-i-do></v-do-i-do>
  </div>
</template>

<script>
import VGraphs from '~/components/organisms/VGraphs'
import VDoIDo from '~/components/organisms/VDoIDo'
import VCareer from '~/components/organisms/VCareer'

export default {
  head: {
    title: 'Career'
  },
  components: {
    VCareer,
    VDoIDo,
    VGraphs
  }
}
</script>
