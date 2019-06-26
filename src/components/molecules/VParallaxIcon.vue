<template>
  <v-parallax :src="src" height="300">
    <v-layout column align-center justify-center class="white--text">
      <h1 class="white--text mb-2 display-1 text-xs-center">{{ title }}</h1>
      <div v-if="subTitle" class="subheading mb-3 text-xs-center">
        {{ subTitle }}
      </div>
      <v-btn class="red mt-5" dark large :to="link">{{ btnText }}</v-btn>
    </v-layout>
  </v-parallax>
</template>

<script>
export default {
  props: {
    src: {
      type: Function,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    subTitle: {
      type: String,
      default: null
    },
    link: {
      type: String,
      required: true
    },
    btnText: {
      type: String,
      required: true
    }
  }
}
</script>

<style></style>
