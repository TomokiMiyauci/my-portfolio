<template>
  <v-card class="elevation-0 transparent">
    <v-card-text class="text-xs-center">
      <v-icon x-large class="red--text">{{ icon }}</v-icon>
    </v-card-text>
    <v-card-title primary-title class="layout justify-center">
      <div class="headline text-xs-center">{{ title }}</div>
    </v-card-title>
    <v-card-text>{{ text }}</v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: null
    },
    title: {
      type: String,
      required: true
    },
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<style></style>
