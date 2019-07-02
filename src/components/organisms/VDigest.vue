<template>
  <v-layout column wrap class="my-5" align-center>
    <v-flex xs12 sm4 class="my-3">
      <div class="text-xs-center">
        <h2 class="headline">Simple and easy development</h2>
        <span class="subheading">Quick overview</span>
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
        title: 'Material Design',
        text:
          'This site uses Vuetify and is made of material design.Vuetify is a fully featured development framework that provides you with everything you need to take any idea from conception to production.'
      },
      {
        icon: 'view_module',
        title: 'Component System',
        text:
          'This site build on Vue.js.Vue is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable.'
      },

      {
        icon: 'flash_on',
        title: 'Fast Deploy',
        text:
          'Deployment is quick and easy using Netlify. In addition to Netlify, there are options such as Github pages and Google Firebase, but Netlify cooperates with Github and can fire a build command triggered by a push to a certain branch (for example, master branch).'
      }
    ],
    type: null
  })
}
</script>

<style></style>
