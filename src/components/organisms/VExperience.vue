<template>
  <v-container grid-list-xl>
    <p class="text-xs-center headline">- Specific -</p>
    <v-layout row wrap justify-space-around>
      <v-flex v-for="i in item" :key="i.name" xs12 sm6 md4 xl4>
        <v-card-rating :i="i"></v-card-rating>
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
    item: [
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
            subtitle: 'Most Use Backend'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/drf.png'),
            title: 'Django Rest Framework',
            subtitle: 'Provide Web API for RESTful - The most Use Backend'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/bs4.jpg'),
            title: 'Beautiful soup4',
            subtitle:
              "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have yo"
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
            subtitle: 'Most Use Backend'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/vuetify.webp'),
            title: 'Vuetify',
            subtitle: 'Provide Web API for RESTful - The most Use Backend'
          },
          { divider: true, inset: true },
          {
            avatar: require('~/assets/img/nuxt.png'),
            title: 'Nuxt.js',
            subtitle:
              "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have yo"
          }
        ]
      }
    ],
    reviews: 'year',
    value: 1.5,
    items: [
      { header: 'Frameworks' },
      {
        avatar: require('~/assets/img/django.png'),
        title: 'Django',
        subtitle: 'Most Use Backend'
      },
      { divider: true, inset: true },
      {
        avatar: require('~/assets/img/drf.png'),
        title: 'Django Rest Framework',
        subtitle: 'Provide Web API for RESTful - The most Use Backend'
      },
      { divider: true, inset: true },
      {
        avatar: require('~/assets/img/bs4.jpg'),
        title: 'Beautiful soup4',
        subtitle:
          "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have yo"
      }
    ]
  }),
  methods: {
    click() {}
  }
}
</script>
