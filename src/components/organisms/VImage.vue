<template>
  <v-parallax-icon v-bind="item"></v-parallax-icon>
</template>

<script>
import VParallaxIcon from '~/components/molecules/VParallaxIcon'
export default {
  components: {
    VParallaxIcon
  },
  data() {
    return {
      item: {
        src: require('assets/logo/load1.jpg'),
        title: 'Who I am.',
        subTitle: "Let's getting start to know about Me!",
        link: '/career',
        btnText: 'Look Career'
      }
    }
  }
}
</script>

<style></style>
