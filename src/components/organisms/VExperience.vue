<template>
  <v-container grid-list-xl>
    <p class="text-xs-center headline">Specific</p>
    <v-layout row wrap justify-space-around>
      <v-flex v-for="item in items" :key="item.name" xs12 sm6 md4 xl4>
        <v-card-rating :items="item"></v-card-rating>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import VCardRating from '~/components/molecules/VCardRating'
export default {
  components: {
    VCardRating
  },
  data: () => ({
    items: [
      {
        name: 'Python',
        src: require('~/assets/logo/python.jpg'),
        value: 1.5,
        version: '3.7.2',
        subItems: [
          { header: 'Ecosystem' },
          {
            avatar: require('~/assets/img/django.png'),
            title: 'Django',
            subtitle:
              'The most used Framework. Especially, ORM and Django SHELL'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/drf.png'),
            title: 'Django Rest Framework',
            subtitle: 'Provide Web API for RESTful - The most Used library'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/bs4.jpg'),
            title: 'Beautiful soup4',
            subtitle:
              'If Web API is not provided or there is only a paid API, it is useless.'
          }
        ]
      },
      {
        name: 'Javascript',
        value: 1.0,
        version: 'ES6',

        src: require('~/assets/logo/javascript.png'),
        subItems: [
          { header: 'Ecosystem' },
          {
            avatar: require('~/assets/img/vue.png'),
            title: 'Vue.js',
            subtitle: 'Awesome component system. SPA can be built easily.'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/vuetify.webp'),
            title: 'Vuetify',
            subtitle: 'Provide a variety of components.'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/nuxt.png'),
            title: 'Nuxt.js',
            subtitle: 'Framework for creating Vue.js applications.'
          }
        ]
      }
    ]
  })
}
</script>
