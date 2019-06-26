<template>
  <v-card>
    <v-img :src="item.src" :aspect-ratio="16 / 9"></v-img>
    <v-card-title>
      <span class="headline">{{ item.name }}</span>
    </v-card-title>
    <v-card-text>
      <span>{{ item.discrib }}</span>

      <v-expansion-panel popout>
        <v-expansion-panel-content
          v-for="subItem in item.subItems"
          :key="subItem.name"
        >
          <template v-slot:header>
            <v-subheader>{{ subItem.name }}</v-subheader>
          </template>
          <v-card>
            <v-card-text>{{ subItem.text }}</v-card-text>
          </v-card>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style></style>
