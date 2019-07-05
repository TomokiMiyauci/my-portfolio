<template>
  <v-hover>
    <v-card>
      <v-img :src="item.src" :aspect-ratio="16 / 9"></v-img>
      <v-card-title>
        <span class="headline">{{ item.name }}</span>
        <v-btn v-if="item.isLink" falt icon>
          <a :href="item.link" target="_blank">
            <v-icon color="primary">exit_to_app</v-icon>
          </a>
        </v-btn>
      </v-card-title>
      <v-card-text>
        <v-chip
          v-for="chip in item.chips"
          :key="chip.text"
          :color="chip.color"
          :text-color="chip.textColor"
          >{{ chip.text }}</v-chip
        >
        <p class="subheading">{{ item.discrib }}</p>

        <v-expansion-panels popout>
          <v-expansion-panel
            v-for="subItem in item.subItems"
            :key="subItem.name"
          >
            <v-expansion-panel-header>
              {{ subItem.name }}
            </v-expansion-panel-header>

            <v-expansion-panel-content>{{
              subItem.text
            }}</v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-card-text>
    </v-card>
  </v-hover>
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

<style scoped>
a {
  text-decoration: none;
}
</style>
