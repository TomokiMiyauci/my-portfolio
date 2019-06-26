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
        src: require('assets/logo/load.jpg'),
        title: 'Who I am.',
        subTitle: "Let's getting start to know about Me!",
        link: '/carrer',
        btnText: 'Look Career'
      }
    }
  }
}
</script>

<style></style>
