<template>
  <v-container grid-list-xl pa-5>
    <p class="text-xs-center headline">- Specific -</p>
    <v-layout row wrap pa-5 justify-space-around>
      <v-flex v-for="i in item" :key="i.name" xs4>
        <v-hover>
          <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`">
            <v-img :aspect-ratio="16 / 9" :src="i.src">
              <v-expand-transition>
                <div
                  v-if="hover"
                  class="d-flex transition-fast-in-fast-out black darken-2 v-card--reveal display-3 white--text"
                  style="height: 100%;"
                >
                  {{ i.version }}
                </div>
              </v-expand-transition>
            </v-img>

            <v-card-title>
              <div>
                <span class="headline">{{ i.name }}</span>
                <div class="d-flex">
                  <v-rating
                    :value="i.value"
                    color="amber"
                    dense
                    half-increments
                    readonly
                    size="20"
                  ></v-rating>
                  <div class="ml-2 grey--text text--darken-2">
                    <span>{{ i.value }}</span>
                    <span>(year)</span>
                  </div>
                </div>
              </div>
            </v-card-title>
            <v-card-text>
              <v-list two-line>
                <template v-for="(item, index) in i.subItems">
                  <v-subheader v-if="item.header" :key="item.header">{{
                    item.header
                  }}</v-subheader>

                  <v-divider
                    v-else-if="item.divider"
                    :key="index"
                    :inset="item.inset"
                  ></v-divider>

                  <v-list-tile v-else :key="item.title" avatar @click="click">
                    <v-list-tile-avatar>
                      <img :src="item.avatar" />
                    </v-list-tile-avatar>

                    <v-list-tile-content>
                      <v-list-tile-title
                        v-html="item.title"
                      ></v-list-tile-title>
                      <v-list-tile-sub-title
                        v-html="item.subtitle"
                      ></v-list-tile-sub-title>
                    </v-list-tile-content>
                  </v-list-tile>
                </template>
              </v-list>
            </v-card-text>
          </v-card>
        </v-hover>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
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

<style scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
</style>
