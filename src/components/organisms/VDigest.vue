<template>
  <v-layout column wrap class="my-5" align-center>
    <v-flex xs12 sm4 class="my-3">
      <div class="text-xs-center">
        <h2 class="headline">The best way to start developing</h2>
        <span class="subheading">Cras facilisis mi vitae nunc</span>
      </div>
    </v-flex>
    <v-flex xs12>
      <v-container grid-list-xl>
        <v-layout row wrap align-center>
          <v-flex v-for="item in items" :key="item.title" xs12 md4>
            <v-card-icon-text
              :icon="item.icon"
              :title="item.title"
              :text="item.text"
            ></v-card-icon-text>
          </v-flex>
        </v-layout>
      </v-container>
    </v-flex>
  </v-layout>
</template>

<script>
import VCardIconText from '~/components/molecules/VCardIconText'
export default {
  components: {
    VCardIconText
  },
  data: () => ({
    items: [
      {
        icon: 'color_lens',
        title: 'hello',
        text:
          'Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt.Suspendisse potenti.'
      },
      {}
    ],
    type: null
  })
}
</script>

<style></style>
